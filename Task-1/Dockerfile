# Use nginx as the base image to serve static files
FROM nginx:alpine

# Copy the HTML and CSS files to the nginx html directory
COPY index.html /usr/share/nginx/html/
COPY styles.css /usr/share/nginx/html/

# Expose port 80
EXPOSE 80
