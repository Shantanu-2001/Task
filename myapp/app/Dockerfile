# Use an official Ruby runtime as the base image
FROM ruby:2.7

# Set the working directory inside the container
WORKDIR /app

# Install Rails and other dependencies
RUN gem install rails bundler

# Copy the Gemfile and Gemfile.lock into the container
COPY Gemfile Gemfile.lock ./

# Install gems
RUN bundle install

# Copy the application code into the container
COPY . .

# Expose the Rails application port (adjust this if necessary)
EXPOSE 3000

# Start the Rails application
CMD ["rails", "server", "-b", "0.0.0.0"]
