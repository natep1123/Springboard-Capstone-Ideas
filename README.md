1. Ecommerce Platform for Gems and Minerals

**Notes:** directory website (like yellow pages), (examples: [archery-range.org](archery-range.org), dog-parks.org)

**Summary:**

Ecommerce marketplace for gems and minerals. Etsy-like platform where users can create shops to sell their gems and minerals, discuss mining/rockhounding in forums and more. Users can bring their rock businesses to this one-stop platform to expand their reach.

**Key Features:**

1. User Shops

- Create customizable shops

- Product listings

- Shops contain blog section for posting

- Product Search

- Filters like: mineral type, price, origin, size, use

- Auctions

- Traditional Online Auctions: set starting bid and duration; buyers bid with outbid notifications.

- Livestream Auctions: Shops can host real-time video auctions with live bidding and chat.

- Community & Education

- Forums for discussing gems/minerals, rockhounding, sourcing, ethics, etc.

- Learning hub with articles, videos, tips for buyers and sellers (e.g., mineral grading, spotting fakes).

- Potentially connect to [mindat.org](mindat.org) API (requires special permission)

**User Flow:**

1. **Onboarding**: User downloads app or visits website, signs up (email/password or social login), sets profile (name, optional seller/buyer role).

2. **Home Screen**: Browse featured shops, products, auctions, or shop blogs. Access search, forums, learning hub, or user profile.

3. **Shop Creation (Sellers)**: Select “Create Shop.” Customize shop (name, banner, description). Add product listings (photos, mineral type, price, origin, size, use).

4. **Shop Blog (Sellers)**: Access blog section in shop dashboard. Create, edit, or delete posts (text, images, videos) about sourcing, rockhounding stories, or shop updates. Publish posts for buyers to view.

5. **Product Search (Buyers)**: Enter keywords or use filters (mineral type, price, origin, size, use). View results with shop details, product listings, and link to the shop's blog.

6. **Traditional Auction (Buyers/Sellers)**: Seller sets starting bid and duration for a listing. Buyers place bids, receive outbid notifications. Highest bidder wins at auction end.

7. **Livestream Auction (Buyers/Sellers)**: Seller hosts real-time video auction. Buyers join, bid via app, and chat. Highest bidder wins when the auction closes.

8. **Purchase**: Buyers add products to cart from shops or auctions. Complete payment (card, PayPal). Seller receives order notification.

9. **Community Engagement**: Access forums to discuss gems, rockhounding, ethics. Post or comment on threads.

10. **Learning Hub**: Browse articles, videos, or tips (e.g., mineral grading, spotting fakes). Optional mindat.org API integration for mineral data (if permitted).

11. **Blog Browsing (Buyers)**: Visit shop’s profile to read blog posts. Engage with posts via comments or shares (optional).

12. **Profile Management**: View purchase/sale history, manage shop listings, track bids, update profile, or manage blog posts.

2. OnTrail

**Summary:**

A journal-first app for outdoor enthusiasts to log adventures with timestamped updates, photos, and gear tracking. Optional "AdventureSync" safety feature shares real-time updates with an emergency contact, aiding rescue efforts if needed. Combines personal reflection with safety for hikers, campers, and adventurers.

**Key Features:**

1. Adventure Logging

- Create time-stamped logs for outdoor activities (e.g., hiking, camping).

- Add updates with text (terrain, personal notes) and optional photos.

- Log start/end points, expected return time, activity type and gear taken.

- Gear Tracking

- Centralized storage for user gear (e.g., boots, backpack, tent).

- Optional gear selection when starting a new adventure log.

- Track gear usage across adventures for personal organization.

- AdventureSync Safety Option

- Optional prompt at adventure start: enable real-time updates to an emergency contact.

- Shares log details (location, timestamps, gear, notes) with contact.

- Enhances safety by providing rescue teams with critical info (e.g., last known location, resources).

- Journal-First Focus

- Narrative logging for personal reflection or sharing (e.g., terrain challenges, wildlife sightings).

- Multimedia support (photos and potential video uploads).


- Weather Tracking (OpenWeatherMap API)

- Log basic current weather (temperature, humidity) with each update

- Display forecasts (hourly and daily) for planning

- Severe weather warnings

**Potential Enhancements:** 

- Log summarization with AI in a neat format for easy social-media posting

- Offline GPS caching for no-service areas.

- Analytics dashboard (e.g., total miles hiked, frequent gear used).

- Community features (e.g., share tips, connect with other adventurers).

**User Flow:**

- **Onboarding:** User downloads app, signs up (email/password or social login), sets profile (name, emergency contact).  

- **Home Screen:** View past adventures or start a new one. Option to manage gear.  

- **Start Adventure:** Tap "New Adventure." Enter activity (e.g., hiking), start/end points, expected return time. Optionally select gear from stored list.  

- **AdventureSync Prompt:** "Enable AdventureSync?" If yes, confirm emergency contact to receive updates.  

- **Logging:** Add updates (text, photos) with timestamps. Auto-log basic weather (temperature, precipitation). Severe weather alerts appear if applicable.  

- **End Adventure:** Mark adventure complete. Log final timestamp and weather. Updates sync to emergency contact if AdventureSync enabled.  

- **Review/Share:** View adventure log (timeline, photos, gear used). Choose to keep private or share publicly (optional).  

- **Gear Management:** Add/edit gear in centralized storage anytime for future adventures.

## 3. Card-io

**Summary:**

A gamified fitness web app that delivers randomized bodyweight workout challenges using a 52-card deck. Each suit maps to a muscle group (push, pull, legs, core), with consistent, hardcoded exercises for progress tracking and shuffled cards for randomization. Users can scale difficulty and monitor stats, with future custom workout creation.

**Key Features:**

1. Workout Challenges

- Assign hardcoded exercises to suits/cards (number: 2-12 reps, royals: 10 reps, aces: 30/45/60 seconds).

- Support full (52 cards) or half (26 cards) decks with multipliers (1x, 2x, 3x).

- Track reps, time, and skips in a summary.

- Card Drawing

- Fetch and shuffle decks via Deck of Cards API, stored in sessionStorage.

- Draw cards to reveal exercises, with skip/tap-out options.

- Custom Workouts (Future)

- Allow users to input custom exercises, reps, and suit assignments.

- Potential AI integration (e.g., xAI Grok API) for tailored workout generation.

- Stats Tracking

- Display workout metrics (reps, time, skips) in a summary view.

- Persist session data via sessionStorage for continuity.

- About Page

- Tabbed UI (Original, Custom) explaining workout modes and challenge details.

**User Flow:**

1. **Onboarding:** User visits website, views homepage with Start Workout or About options.

2. **Start Workout:** Select deck size (full/half) and multiplier (1x/2x/3x) in a form.

3. **Workout:** Draw cards to reveal exercises, perform reps/time, skip or tap out. View real-time stats (cards remaining, time).

4. **Summary:** After completion, view stats (reps, time, skips). Reset to start a new workout.

5. **About Page:** Information page about the deck of cards challenge and interface.

6. **Custom Workout (Future):** Access form to input exercises, save to sessionStorage, and use in workouts.
