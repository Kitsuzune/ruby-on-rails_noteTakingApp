# Fasih Note Taking App Interview Solution

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Ruby 3.2.3** (Required)
- **Rails 7.x**

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/Kitsuzune/ruby-on-rails_noteTakingApp.git
cd ruby-on-rails_noteTakingApp/fasihIn
```

### 2. Install Ruby 3.2.3

If you don't have Ruby 3.2.3 installed, you can install it using a Ruby version manager:

#### Using rbenv:
```bash
rbenv install 3.2.3
rbenv local 3.2.3
```

#### Using RVM:
```bash
rvm install 3.2.3
rvm use 3.2.3
```

### 3. Install Dependencies

```bash
# Install Ruby gems
bundle install
```

## Running the Application

### Development Server

```bash
rails server
```

The application will be available at `http://localhost:3000`

### Alternative Port

```bash
rails server -p 4000
```

## Usage

1. **Home Page**: Navigate to `http://localhost:3000/` to see all notes
2. **Create Note**: Click "New Note" button to create a new note
3. **View Note**: Click "Show" to view a specific note
4. **Edit Note**: Click "Edit" to modify an existing note
5. **Delete Note**: Click "Delete" and confirm to remove a note

## Database Schema

The application uses a simple Note model with the following attributes:

- `id`: Primary key (integer)
- `title`: Note title (string)
- `content`: Note content (text)
- `created_at`: Creation timestamp
- `updated_at`: Last update timestamp

## Project Structure

```
app/
├── controllers/
│   └── notes_controller.rb    # Main controller handling CRUD operations
├── models/
│   └── note.rb               # Note model
├── views/
│   └── notes/
│       ├── index.html.erb    # List all notes
│       ├── show.html.erb     # Display single note
│       ├── new.html.erb      # Create new note form
│       └── edit.html.erb     # Edit note form
config/
├── routes.rb                 # Application routes
└── database.yml             # Database configuration
db/
├── migrate/
│   └── 20250719040004_create_notes.rb
└── schema.rb
```

## Available Routes

| HTTP Method | Path | Controller#Action | Description |
|-------------|------|-------------------|-------------|
| GET | /notes | notes#index | List all notes |
| GET | /notes/new | notes#new | Show new note form |
| POST | /notes | notes#create | Create new note |
| GET | /notes/:id | notes#show | Show specific note |
| GET | /notes/:id/edit | notes#edit | Show edit note form |
| PATCH/PUT | /notes/:id | notes#update | Update note |
| DELETE | /notes/:id | notes#destroy | Delete note |

## Troubleshooting

### Common Issues

1. **Ruby Version Mismatch**: Make sure you're using Ruby 3.2.3
   ```bash
   ruby -v
   # Should output: ruby 3.2.3
   ```

2. **Database Issues**: If you encounter database errors:
   ```bash
   rails db:drop
   rails db:create
   rails db:migrate
   ```

3. **Asset Issues**: If styles don't load properly:
   ```bash
   rails assets:clean
   rails assets:precompile
   ```

4. **Bundle Issues**: If gems are not installing:
   ```bash
   bundle clean --force
   bundle install
   ```

### Alternative Port

If you want to run on a different port:

```bash
rails server -p 4000
```

## Usage

1. **Home Page**: Navigate to `http://localhost:3000/notes` to see all notes
2. **Create Note**: Click "New Note" button to create a new note
3. **View Note**: Click "Show" to view a specific note
4. **Edit Note**: Click "Edit" to modify an existing note
5. **Delete Note**: Click "Delete" and confirm to remove a note

## Database Schema

The application uses a simple Note model with the following attributes:

- `id`: Primary key (integer)
- `title`: Note title (string)
- `content`: Note content (text)
- `created_at`: Creation timestamp
- `updated_at`: Last update timestamp

## Project Structure

```
app/
├── controllers/
│   └── notes_controller.rb    # Main controller handling CRUD operations
├── models/
│   └── note.rb               # Note model
├── views/
│   └── notes/
│       ├── index.html.erb    # List all notes
│       ├── show.html.erb     # Display single note
│       ├── new.html.erb      # Create new note form
│       └── edit.html.erb     # Edit note form
config/
├── routes.rb                 # Application routes
└── database.yml             # Database configuration
db/
├── migrate/
│   └── 20250719040004_create_notes.rb
└── schema.rb
```

## Available Routes

| HTTP Method | Path | Controller#Action | Description |
|-------------|------|-------------------|-------------|
| GET | /notes | notes#index | List all notes |
| GET | /notes/new | notes#new | Show new note form |
| POST | /notes | notes#create | Create new note |
| GET | /notes/:id | notes#show | Show specific note |
| GET | /notes/:id/edit | notes#edit | Show edit note form |
| PATCH/PUT | /notes/:id | notes#update | Update note |
| DELETE | /notes/:id | notes#destroy | Delete note |

## Testing

To run the test suite:

```bash
# Run all tests
rails test

# Run specific test files
rails test test/models/note_test.rb
rails test test/controllers/notes_controller_test.rb
```

## Troubleshooting

### Common Issues

1. **Ruby Version Mismatch**: Make sure you're using Ruby 3.2.3
   ```bash
   ruby -v
   # Should output: ruby 3.2.3
   ```

2. **Database Issues**: If you encounter database errors:
   ```bash
   rails db:drop
   rails db:create
   rails db:migrate
   ```

3. **Asset Issues**: If styles don't load properly:
   ```bash
   rails assets:clean
   rails assets:precompile
   ```

4. **Bundle Issues**: If gems are not installing:
   ```bash
   bundle clean --force
   bundle install
   ```
