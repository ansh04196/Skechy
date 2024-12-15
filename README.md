# Sketchy

**Sketchy** is a real-time collaborative platform designed to facilitate teamwork through interactive whiteboards, drawing tools, shapes, and more. This workspace is ideal for brainstorming sessions, planning, and collaborative design.

## Screenshots

![Login](./public/Sketchy%20Login.png)
![Dashboard](./public/Sketchy%20Dashboard.png)
![Drawboard](./public/Sketchy%20Drawboard.png)
![Invite](./public/Sketchy%20Invite.png)
![Loading](./public/Sketchy%20Loading.png)

## Tech Stack

- **Framework**: [Next.js](https://nextjs.org/)
- **UI Components**: [shadcn/ui](https://ui.shadcn.com/)
- **Backend**: [convex](https://www.convex.dev/)
- **Real-time Collaboration**: [liveblocks](https://liveblocks.io/)

## Deployment

The application is deployed on Vercel. Check it out [here](https://skechy.vercel.app/).

## Getting Started

Follow these instructions to set up Sketchy locally.

### Prerequisites

Ensure you have the following installed on your system:

- Node.js (>= 14.x)
- npm

### Installation

1. **Clone the repository:**

   ```sh
   git clone https://github.com/ansh04196/Skechy.git
   cd sketchy
   ```

2. **Install dependencies:**

   ```sh
   npm install
   ```

3. **Configure environment variables:**

   Create a `.env.local` file in the root directory and add your configuration variables. You can explore the `.env.example` file for more information.

4. **Clerk Setup**

   - Enable Organization from the "Organization settings"
   - Add a JWT Template named "convex"
   - Ensure `org_id` and `org_role` are inside **Claims**
   - Add the issuer into the `auth.config.js` inside `/convex`.

5. **Prepare the convex functions:**

   ```sh
   npx convex dev
   ```

6. **Run the development server:**

   ```sh
   npm run dev
   ```

   Open [http://localhost:3000](http://localhost:3000) in your browser to see the result.

## Features

- **Real-time Collaboration**: Collaborate with team members in real time to build and refine automated workflows.
- **Interactive UI**: An intuitive and responsive user interface for seamless workflow creation and management.
- **Scalable Backend**: Powered by Convex for efficient backend logic and data storage.
- **Live Updates**: Instant updates using Liveblocks for real-time synchronization across users.

### New Features

- **Keyboard Shortcuts**:

  - **Move Selected Items**: Use keyboard shortcuts to move selected items within the workspace.
  - **Duplicate Items**: Duplicate selected items with `Ctrl + D`.
  - **Focus Search Input**: Quickly focus on the search input field using a keyboard shortcut.

- **Enhanced Workflow Tools**:

  - **Improved Layout and Functionality**: Added icons and shortcuts for easier workflow management.
  - **Precise Selection**: Items are selected only when fully enclosed within the selection area.

- **Workflow Limits**:

  - Users can create up to 5 workflows per organization to ensure efficient management.

- **Reset View**:

  - A reset button appears when scrolling through the workspace, allowing users to quickly return to the default view.

- **Customizable Elements**:

  - Utilize the color picker with debouncing to prevent unnecessary undo/redo actions and enable infinite color combinations for your workflow elements.

- **Export as PNG**:

  - Export your workflow as a PNG image file to share or archive your work easily.
