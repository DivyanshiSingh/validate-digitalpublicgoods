[![License: GPL v3](https://img.shields.io/badge/License-GPL%20v3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0) [![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-v2.0%20adopted-ff69b4.svg)](code_of_conduct.md)

# Validate Digital Public Goods App

The [Digital Public Goods Alliance](https://digitalpublicgoods.net/) is now crowdsourcing reviews of digital public goods! We’re asking you to participate by reviewing open source projects against the [Digital Public Goods Standard](https://digitalpublicgoods.net/standard) with the ultimate goal of determining if a project qualifies as a Digital Public Good.

## 💡 Motivation

Open source represents an unprecedented opportunity to fundamentally alter power balances in international development. But, we can’t harness that power without the cooperation of many - reviewers, maintainers, creators, policy makers, and so many others (that means you! 👊).

This community sourcing exercise will give you the opportunity to delve into some of the largest up and coming open source projects. You’ll get a chance to understand their licenses and documentation, and how they’re designing for best practices, standards, privacy and more.

By participating, you’ll get a better understanding of open projects that are making a difference in the world, particularly those that are advancing practical solutions to help achieve the Sustainable Development Goals (SDGs). You’ll also join a growing number of innovators working on technology for development (T4D).

## 🎮 App

The app is live at https://validate.digitalpublicgoods.net for anyone to contribute!

## 💻 Development Environment

### 1. Clone the repository and install dependencies

```
git clone https://github.com/lacabra/validate-digitalpublicgoods.git
cd validate-digitalpublicgoods
npm i
```

### 2. Configure your local environment

1. Copy the .env.local.example file in this directory to .env.local (which will be ignored by Git):

    ```
    cp .env.local.example .env.local
    ```

2. Clone [unicef/publicgoods-candidates](https://github.com/unicef/publicgoods-candidates) to your personal account and set the following variables in `.env.local`:
    ```
    NEXT_PUBLIC_GITHUB_OWNER="YOUR_GITHUB_USERNAME"
    NEXT_PUBLIC_GITHUB_REPO=publicgoods-candidates
    ```

3. Create your [GitHub OAuth App](https://docs.github.com/en/developers/apps/creating-an-oauth-app), and set the following variables in `.env.local`:
    ```
    GITHUB_ID=
    GITHUB_SECRET=
    ```

### 3. Start the application

To run your site locally, use:

```
npm run dev
```

To run it it production mode, use:

```
npm build
npm start
```

### 4. Configuring for production

You must set the NEXTAUTH_URL environment variable with the URL of your site, before deploying to production.

e.g. `NEXTAUTH_URL=https://example.com`

To do this in on Vercel, you can use the [Vercel project dashboard](https://vercel.com/dashboard) or the `now env` command:

    now env add NEXTAUTH_URL production

Be sure to also set environment variables for the Client ID and Client Secret values for all your authentication providers.

## :memo: License

This software is licensed under the [GNU General Public License](LICENSE) as published by the Free Software Foundation, either version 3 of the License, or
any later version.

```
    ProjectConnect App
    Copyright (C) 2020 UNICEF

    This program is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License as published by
    the Free Software Foundation, either version 3 of the License, or
    (at your option) any later version.

    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.

    You should have received a copy of the GNU General Public License
    along with this program.  If not, see <https://www.gnu.org/licenses/>.
```
