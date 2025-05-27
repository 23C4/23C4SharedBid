
# Online Bidding Platform

An interactive web application for online auctions where users can bid on products and participate in collaborative bidding.

## Project Structure

### Core Files

- `src/main.tsx`: Entry point of the application
- `src/App.tsx`: Main component that sets up routing and providers
- `src/index.css`: Global styles using Tailwind CSS

### Folders

#### `/components`

Contains reusable UI components:

- `Navbar.tsx`: Navigation bar shown on all pages
- `ProductCard.tsx`: Card component for displaying product information
- `ProductGrid.tsx`: Grid layout for displaying multiple products
- `BiddingHistory.tsx`: Component for showing bid history on a product
- `CollaborativeBidCard.tsx`: Card for collaborative bidding information
- `StatCard.tsx`: Shows statistics on dashboard
- `/ui`: UI components from shadcn/ui library (buttons, cards, dialogs, etc.)

#### `/context`

Contains React context providers for state management:

- `AuthContext.tsx`: Manages user authentication state including login/registration
- `ProductContext.tsx`: Manages products, bids, and collaborative bidding data

#### `/hooks`

Custom React hooks:

- `use-mobile.tsx`: Hook for detecting mobile viewport
- `use-toast.ts`: Hook for displaying toast notifications

#### `/lib`

Utility functions:

- `utils.ts`: Generic utility functions for the application

#### `/pages`

Page components:

- `Index.tsx`: Landing page
- `Login.tsx`: User login page
- `Register.tsx`: User registration page
- `BidderHome.tsx`: Home page for bidders showing available products
- `SellerHome.tsx`: Home page for sellers showing their listings
- `Dashboard.tsx`: User dashboard with statistics
- `ProductDetail.tsx`: Detailed view of a product with bidding functionality
- `NotFound.tsx`: 404 page

#### `/types`

TypeScript type definitions:

- `index.ts`: Contains interfaces for User, Product, Bid, and CollaborativeBid

## Data Flow

1. User data is managed by `AuthContext` and stored in localStorage
2. Product and bidding data is managed by `ProductContext` and stored in localStorage
3. Components use the context hooks to access and update data
4. Pages display data using the reusable components

## Features

- **User Authentication**: Login and registration for bidders and sellers
- **Product Listings**: View available products with details and current bids
- **Bidding**: Place bids on products
- **Collaborative Bidding**: Join forces with other users to bid on expensive items
- **Dashboard**: View statistics and activity
- **Persistent Storage**: All data is stored in localStorage for persistence

## How to Run Locally

### Requirements

- Node.js (v16+)
- npm, yarn, or bun

### Installation Steps

1. Clone the repository
```bash
git clone <repository-url>
cd online-bidding-platform
```

2. Install dependencies
```bash
npm install
# or
yarn install
# or
bun install
```

3. Start the development server
```bash
npm run dev
# or
yarn dev
# or
bun dev
```

4. Open your browser and navigate to `http://localhost:5173`

### Login Information

You can use these pre-configured accounts to test the application:

- **Seller Account**: 
  - Email: seller@example.com
  - Role: seller

- **Bidder Account**:
  - Email: bidder@example.com
  - Role: bidder

No password is required in this demo version, just enter the email and select the correct role.

You can also register new accounts through the registration page.

## Data Persistence

The application uses localStorage to persist data between sessions, including:
- User accounts
- Current user session
- Products
- Bids
- Collaborative bids

This means your data will remain even after refreshing the browser or closing the application.
