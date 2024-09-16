# Use the official Node.js 16 image.
# https://hub.docker.com/_/node
FROM node:18.20.4-alpine

# Create a directory for our app.
# Ensure the directory name is all lowercase to comply with npm naming restrictions.
RUN mkdir -p /usr/src/app/luping_xing
WORKDIR /usr/src/app/luping_xing

# Install Create React App globally.
RUN npm install -g create-react-app

# Initialize a new React application with a valid name.
# Using a generic name like 'app' to avoid npm naming issues.
RUN create-react-app app

# Navigate into the newly created app directory.
WORKDIR /usr/src/app/luping_xing/app

# Replace the default src/App.js with our custom content.
RUN echo "import React from 'react';" > src/App.js
RUN echo "function App() {" >> src/App.js
RUN echo "  return (" >> src/App.js
RUN echo "    <div className='App'>" >> src/App.js
RUN echo "      <header className='App-header'>" >> src/App.js
RUN echo "        <h1>Codin 1</h1>" >> src/App.js
RUN echo "      </header>" >> src/App.js
RUN echo "    </div>" >> src/App.js
RUN echo "  );" >> src/App.js
RUN echo "}" >> src/App.js
RUN echo "export default App;" >> src/App.js

# Expose the port the app runs on.
EXPOSE 7775

# Set environment variable for the port and start the app using the development server.
ENV PORT=7775
CMD ["npm", "start"]