![Image](/public/image.png)
# Bet

A forum built for Gen Z thrill-seekers where users can post, accept, and track community challenges.

## Features

* **Full CRUD Operations:** Seamlessly create, read, update, and delete challenge posts in real time.
* **Supabase Integration:** Powered by a reliable PostgreSQL database backend using Supabase for persistent data storage.
* **Dynamic Challenge Feed:** All submitted community challenges are instantly fetched and ordered by creation date on the homepage.
* **Interactive Bet Tracking:** A real-time counter that tracks and updates how many users have accepted each specific challenge.

---

## Installation

### Prerequisites

Before running the application, make sure you have the following installed on your machine:

* **Node.js:** v18.0.0 or higher
* **npm:** v9.0.0 or higher
* A **Supabase** account and an active database project.

### Step-by-step Setup

1. **Clone the repository:**
```bash
git clone git@github.com:YOUR-USERNAME/web102_unit7lab.git
cd web102_unit7lab

```


2. **Install dependencies:**
```bash
npm install

```


3. **Configure your Database Client:**
Create a `src/client.js` file in your root directory and connect your Supabase project credentials:
```javascript
import { createClient } from '@supabase/supabase-js'

const URL = 'your_supabase_project_url'
const API_KEY = 'your_supabase_publishable_anon_key'

export const supabase = createClient(URL, API_KEY)

```



---

## Usage

### Running the Application

To launch the React front-end server locally in development mode:

```bash
npm run dev

```

### Database Table Schema

To ensure the application functions correctly, create a `Posts` table in your Supabase database with the following columns:

| Column Name | Data Type | Default Value |
| --- | --- | --- |
| `id` | int8 | *Auto-increment* |
| `created_at` | timestamptz | `now()` |
| `title` | text | `NULL` |
| `author` | text | `NULL` |
| `description` | text | `NULL` |
| `betCount` | numeric | `0` |

---

## Contributing

We welcome and appreciate contributions to the project! Please review our [Contributing Guidelines](https://www.google.com/search?q=CONTRIBUTING.md) for details on our code of conduct, development workflows, and how to submit pull requests.

---

## License

This project is licensed under the MIT License. See the [LICENSE](https://www.google.com/search?q=LICENSE) file for the full license text.