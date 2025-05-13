const fs = require('fs');
const path = require('path');

const componentsDir = path.join(__dirname, 'components');

// Get all directories inside the components directory
const subdirs = fs.readdirSync(componentsDir).filter(item => {
  const itemPath = path.join(componentsDir, item);
  return fs.statSync(itemPath).isDirectory();
});

// Create the associations object
const associations = {};
subdirs.forEach(dir => {
  associations[dir] = 'React-components';
});

// Create the final JSON object
const result = {
  associations
};

console.log(JSON.stringify(result, null, 2));
