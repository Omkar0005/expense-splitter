# Splitr

A modern, full-stack expense splitting application built with Next.js, Convex, and Clerk. Splitr helps you track shared expenses, split bills effortlessly, and settle up quickly with friends and groups.

## Features

- **Group Expenses**: Create groups for roommates, trips, or events to keep expenses organized.
- **Smart Settlements**: Algorithm minimizes the number of payments when settling up.
- **Expense Analytics**: Track spending patterns and discover insights about shared costs.
- **Payment Reminders**: Automated reminders for pending debts and spending insights.
- **Multiple Split Types**: Split equally, by percentage, or by exact amounts.
- **Real-time Updates**: See new expenses and repayments instantly.
- **AI-Powered Insights**: Integrated with Gemini AI for spending insights.
- **Responsive Design**: Built with Tailwind CSS and Shadcn UI for a modern, mobile-friendly interface.

## Tech Stack

- **Frontend**: Next.js 15, React 19, Tailwind CSS, Shadcn UI
- **Backend**: Convex (real-time database and functions)
- **Authentication**: Clerk
- **Background Jobs**: Inngest
- **AI**: Google Generative AI (Gemini)
- **Email**: Resend
- **Icons**: Lucide React
- **Charts**: Recharts

## Prerequisites

- Node.js 18+
- npm or yarn
- Convex account
- Clerk account
- Resend account (for emails)
- Google AI API key (for insights)

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/splitr.git
   cd splitr
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Set up Convex:

   ```bash
   npx convex dev --once
   ```

4. Create a `.env.local` file in the root directory with the following variables:

   ```env
   # Convex
   CONVEX_DEPLOYMENT=
   NEXT_PUBLIC_CONVEX_URL=

   # Clerk Authentication
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
   CLERK_SECRET_KEY=
   NEXT_PUBLIC_CLERK_SIGN_IN_URL=/sign-in
   NEXT_PUBLIC_CLERK_SIGN_UP_URL=/sign-up
   CLERK_JWT_ISSUER_DOMAIN=

   # Email (Resend)
   RESEND_API_KEY=

   # AI (Google Gemini)
   GEMINI_API_KEY=
   ```

5. Seed the database (optional):
   ```bash
   npx convex run seed
   ```

## Running the Application

1. Start the development server:

   ```bash
   npm run dev
   ```

2. Open [http://localhost:3000](http://localhost:3000) in your browser.

3. For production build:
   ```bash
   npm run build
   npm start
   ```

## Usage

1. **Sign Up/Sign In**: Create an account or sign in with Clerk.
2. **Create a Group**: Start a new group and invite friends.
3. **Add Expenses**: Record expenses and specify how to split them.
4. **View Balances**: Check who owes what in the dashboard.
5. **Settle Up**: Log payments when debts are cleared.
6. **Analytics**: Explore spending insights and patterns.

## Project Structure

```
splitr/
├── app/                    # Next.js app router pages
│   ├── (auth)/            # Authentication pages
│   ├── (main)/            # Main app pages
│   └── api/               # API routes
├── components/            # Reusable UI components
├── convex/                # Convex backend functions and schema
├── hooks/                 # Custom React hooks
├── lib/                   # Utility functions and constants
├── inngest/               # Background job functions
└── public/                # Static assets
```

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add some feature'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a pull request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Inspired by Splitwise
- Built following tutorials and best practices from the community
- Icons by Lucide React
- UI components by Shadcn UI
