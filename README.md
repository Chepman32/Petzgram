# Petzgram 🐾

**Instagram-like social network exclusively for pets and their owners**

A React Native CLI + TypeScript application built with Firebase backend, featuring rich animations, social features, and monetization through IAP subscriptions.

## 📱 Platform Support
- **Primary**: iOS 14+
- **Language**: TypeScript
- **Framework**: React Native CLI

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- Xcode 14+ (for iOS development)
- CocoaPods
- Firebase project setup

### Installation & Launch
```bash
# Install dependencies
yarn install

# Install iOS pods
cd ios && pod install && cd ..

# Launch on iPhone 15 Pro simulator
npx react-native run-ios --simulator="iPhone 15 Pro"
```

## 🏗️ Architecture & Tech Stack

### Core Technologies
- **React Native CLI** with TypeScript
- **React Navigation v6** (Stack + Bottom Tabs)
- **React Native Reanimated v3** for 60fps animations
- **Redux Toolkit + Redux Persist** for state management
- **Firebase** (Auth, Firestore, Storage, Functions, Messaging)

### Key Libraries
- `react-native-gesture-handler` - Gesture handling
- `react-native-safe-area-context` - Safe area management
- `react-native-image-picker` - Media selection
- `react-native-fast-image` - Optimized image loading
- `react-native-video` - Video playback
- `react-native-iap` - In-app purchases
- `react-native-vector-icons` - Icon library
- `lottie-react-native` - Lottie animations

## 📋 Feature Implementation Status

### ✅ Implemented Features

#### Core Infrastructure
- [x] **Project Setup**: React Native CLI with TypeScript
- [x] **Navigation**: React Navigation v6 with Stack and Bottom Tabs
- [x] **State Management**: Redux Toolkit with persistence
- [x] **Firebase Integration**: Basic setup ready

### 🚧 In Progress Features

#### Authentication & Onboarding
- [ ] **Animated Splash Screen**: Logo morphing animation with Reanimated
- [ ] **Onboarding Flow**: 3-5 slides with parallax animations
- [ ] **Authentication**: Email/Password, Apple ID, Google Sign-In
- [ ] **Profile Setup**: Pet profile creation with photo upload

#### Main App Features
- [ ] **Bottom Tab Navigation**: Feed, Discover, Post, Clubs, Profile
- [ ] **Feed Screen**: Stories + Posts with infinite scroll
- [ ] **Story System**: Creation, viewing with progress bars
- [ ] **Post Creation**: Multi-media composer with editing
- [ ] **Discovery**: Trending, breed filters, geo-search
- [ ] **Pet Profiles**: Multi-pet support, statistics
- [ ] **Clubs System**: Breed-based communities

### 📅 Planned Features

#### Social Features
- [ ] **Comments System**: Nested replies, mentions
- [ ] **Direct Messaging**: 1:1 and group chats
- [ ] **Follow System**: Following/followers
- [ ] **Likes & Reactions**: Double-tap animations
- [ ] **Content Sharing**: Cross-platform sharing

#### Advanced Features
- [ ] **Map Integration**: Pet-friendly places, services
- [ ] **Events System**: Meetups, playdates
- [ ] **Live Stories**: Real-time story features
- [ ] **Push Notifications**: Engagement notifications
- [ ] **Content Moderation**: Report/block system

#### Monetization
- [ ] **Premium Subscriptions**: Monthly/yearly plans
- [ ] **Post Boosting**: Paid promotion system
- [ ] **Premium Features**: Enhanced discovery, unlimited stories
- [ ] **IAP Integration**: Subscription management

#### Performance & UX
- [ ] **Offline Support**: Cached content, upload queue
- [ ] **Advanced Animations**: Shared element transitions
- [ ] **Accessibility**: VoiceOver, Dynamic Type support
- [ ] **Localization**: Multi-language support

## 🎨 Animation System

### Reanimated v3 Implementations
- **Splash Animation**: Logo morph sequence with confetti
- **Gesture Interactions**: Swipe, pinch, drag gestures
- **Layout Animations**: Mount/unmount transitions
- **Micro-interactions**: Button presses, success states
- **Shared Elements**: Profile to detail transitions

### Performance Targets
- 60fps animations across all interactions
- Smooth scrolling with optimized lists
- Efficient video playback management

## 🗄️ Data Architecture

### Firebase Collections
```
users/{uid}
├── displayName, pets[], photoURL, bio
├── breeds[], geo, counters
└── premium: {active, plan, expiry}

pets/{petId}
├── ownerUid, species, breed, age, sex
├── tags, avatarURL
└── stats: {posts, followers}

posts/{postId}
├── authorUid, petId, media[]
├── caption, breeds[], location
└── likesCount, commentsCount

clubs/{clubId}
├── title, description, breeds[]
├── membersCount, moderators[]
└── rules, coverURL

stories/{uid}/items/{storyId}
├── media, expiresAt
└── viewersCount

chats/{chatId}
├── members[2], lastMessage
└── messages subcollection
```

### Security Rules
- User-owned data protection
- Media access validation
- Rate limiting for posts
- Content moderation triggers

## 💰 Monetization Strategy

### Subscription Tiers
- **Free**: Basic features, limited stories
- **Premium Monthly**: `petzgram.premium.monthly`
- **Premium Yearly**: `petzgram.premium.yearly`

### Premium Features
- View who liked your posts
- Advanced discovery filters
- Unlimited stories
- Priority in discovery
- Premium badge
- Ad-free experience

### Consumables
- Post boost (24h): `petzgram.boost.1`
- Boost packs: 5x, 10x bundles

## 📊 Analytics & Monitoring

### Firebase Analytics Events
- `open_app`, `view_feed`, `like_post`
- `create_post`, `story_view`, `club_join`
- `iap_paywall_view`, `iap_purchase`

### Performance Monitoring
- Crash reporting with Crashlytics
- Performance metrics tracking
- User engagement analytics

## 🔒 Privacy & Security

### Data Protection
- GDPR/CCPA compliance
- Account deletion workflow
- Privacy-first design
- Secure media storage

### Content Safety
- Report/block system
- Automated content moderation
- Community guidelines enforcement
- Safe chat environment

## 🧪 Testing Strategy

### Test Coverage
- **Unit Tests**: Jest for business logic
- **Component Tests**: React Native Testing Library
- **E2E Tests**: Detox for critical flows
- **Performance Tests**: Animation smoothness

### CI/CD Pipeline
- Automated testing on PR
- TestFlight deployment
- Fastlane integration
- Release automation

## 📱 App Store Preparation

### Requirements
- Privacy Nutrition Labels
- Sign in with Apple compliance
- App Store screenshots
- Metadata localization

### Release Process
- Beta testing via TestFlight
- Staged rollout strategy
- Performance monitoring
- User feedback integration

## 🛠️ Development Guidelines

### Code Standards
- TypeScript strict mode
- ESLint + Prettier configuration
- Component-based architecture
- Reusable UI components

### Performance Best Practices
- Image optimization with FastImage
- Video playback management
- List virtualization
- Memory leak prevention

### Animation Guidelines
- 60fps target for all animations
- Gesture-driven interactions
- Meaningful motion design
- Accessibility considerations

## 🤝 Contributing

### Development Workflow
1. Feature branch from `main`
2. Implement with tests
3. Code review process
4. Merge to `main`
5. Deploy to TestFlight

### Code Review Checklist
- TypeScript compliance
- Animation performance
- Accessibility support
- Security considerations

## 📞 Support & Documentation

### Resources
- [React Native Documentation](https://reactnative.dev)
- [Firebase Documentation](https://firebase.google.com/docs)
- [Reanimated Documentation](https://docs.swmansion.com/react-native-reanimated/)

### Project Status
**Current Phase**: Project initialized (RN CLI + TypeScript, base navigation/state scaffolding)
**Next Milestone**: Authentication + Onboarding + Tabs scaffold
**Target Launch**: 2025 H2 (TBD)

## 📌 Feature Status Matrix

Legend: [x] Implemented • [~] In Progress • [ ] Planned

### Core & Platform
- [x] React Native CLI project (TypeScript)
- [x] iOS 14+ target
- [x] Base navigation (React Navigation v6)
- [~] Redux Toolkit + Persist setup
- [ ] RTK Query (Firebase)
- [ ] Reanimated v3 integrated globally

### Authentication & Onboarding
- [ ] Animated Splash (logo morph, preload assets/remote config)
- [ ] Onboarding (3–5 slides, parallax, pager indicator)
- [ ] Sign In/Up (Email/Password)
- [ ] Sign in with Apple
- [ ] Sign in with Google
- [ ] 2FA / Email link (optional)
- [ ] Complete Pet Profile wizard

### App Navigation
- [ ] Root Stack (AuthStack, AppTabs, Modals)
- [ ] Bottom Tabs: Feed, Discover, Post(+), Clubs, Profile
- [ ] Modals: StoryViewer, PostComposer, Filters, Paywall, EditPetProfile, Chat, Map
- [ ] Deep Links: `petzgram://post/:id`, `petzgram://pet/:id`, `petzgram://club/:id`

### Feed & Stories
- [ ] Stories row with avatars → StoryViewer
- [ ] StoryViewer: progress bars, hold-to-pause, swipe-down dismiss
- [ ] Post card: media carousel (1..10), caption, tags, location
- [ ] Double-tap like with heart burst animation
- [ ] Pull-to-refresh with custom indicator
- [ ] Auto-play muted video in viewport (single active)
- [ ] Loading skeletons, empty and error states

### Discover & Map
- [ ] Tabs: Trending, By Breed, Nearby (geo)
- [ ] Filters modal: species/breed/age/sex/radius/hasVideo
- [ ] Map with clustered pins and swipe-up place card
- [ ] Shared layout animation grid ↔ map

### Post (+ Composer)
- [ ] Media source: camera/gallery, multi-select, reorder (drag & drop)
- [ ] Editor: crop, overlays/stickers, breed tags, geo
- [ ] Preview carousel
- [ ] Upload to Storage with progress + optimistic insert
- [ ] Persistent retry queue on network errors

### Clubs
- [ ] Clubs list with online badge, post counters
- [ ] Club screen: banner, description, rules, posts, pin, Join button
- [ ] Club events: list + map
- [ ] Roles: owner/moderator/member + moderator application flow

### Profile
- [ ] Collapsing header (parallax), avatar scale
- [ ] Tabs: Posts / Saved / Tagged / Pets
- [ ] Actions: Edit Profile, Add Pet, Share profile; Follow/Message for others
- [ ] Grid with FastImage + prefetch
- [ ] Stats with count-up animation
- [ ] Multi-pet segmented control

### Post Detail & Comments
- [ ] Media pager with zoom/pan
- [ ] Comments with inline replies, @pet, #breed
- [ ] Long-press actions (copy/report)
- [ ] Bottom composer with send bounce

### Chat
- [ ] Chats list (last message, unread badge)
- [ ] Thread: bubbles, photo/video, reply quote, typing indicator, delivered/read
- [ ] Media upload with progress
- [ ] Report/Block → Firestore + Function

### Firebase & Server Logic
- [ ] Auth providers wired (Email/Apple/Google)
- [ ] Storage paths & rules for posts/stories/pets
- [ ] Firestore Security Rules (RLS, validation, rate limits)
- [ ] Cloud Functions: notifications on like/comment, story TTL, moderation queue, counters denorm
- [ ] Messaging: push notifications (mute options)

### State & Offline
- [~] Redux slices: auth, profile, feed, clubs, chat, iap, notifications
- [ ] Persist critical slices; Firestore offline persistence
- [ ] Upload queue for media (retry)

### Monetization (IAP)
- [ ] Subscriptions: `petzgram.premium.monthly`, `petzgram.premium.yearly`
- [ ] Consumables: Boost `petzgram.boost.1` (packs 5/10)
- [ ] Paywall modal with tiers, localized prices, Restore, Terms/Privacy
- [ ] Premium gating: who-liked-you, advanced filters, unlimited stories, priority discover, badge, remove promos
- [ ] Receipt validation + Firestore flag

### Analytics & Remote Config
- [ ] Events: open_app, view_feed, like_post, create_post, story_view, club_join, iap_paywall_view, iap_purchase
- [ ] Remote Config experiments (feed sort, limits)

### Performance
- [ ] FastImage caching + prefetch
- [ ] Video: single active player, pause off-screen
- [ ] Thumbnails + progressive image loading
- [ ] FlatList/FlashList windowing, memoization

### Accessibility & Safety
- [ ] VoiceOver labels, Dynamic Type, contrast, touch targets
- [ ] Report/Block, content filters, private profile
- [ ] App Tracking Transparency (if ads/attribution)
- [ ] Account deletion (GDPR/CCPA)

### Testing & Release
- [ ] Unit (Jest), component (RNTL), e2e (Detox) for post/comment/IAP flows
- [ ] App Store: screenshots, Privacy Nutrition Labels, Sign in with Apple compliance
- [ ] CI/CD: fastlane (build, TestFlight), release automation

## 🧭 Navigation Map
```
RootStack
├─ AuthStack: Onboarding → SignIn/SignUp → CompleteProfile
├─ AppTabs: Feed | Discover | Post(+) | Clubs | Profile
└─ Modals: StoryViewer | PostComposer | Filters | Paywall | EditPetProfile | Chat | Map
```

## 🔗 Deep Links
- `petzgram://post/:id`
- `petzgram://pet/:id`
- `petzgram://club/:id`

## 📂 Project Structure (proposed)
```
src/
  app/
    navigation/
    store/
    theme/
  features/
    auth/ feed/ discover/ post/ clubs/ profile/ chat/ story/
  components/
  services/ (firebase, iap, analytics)
  utils/
  types/
```

## 🛠 Scripts
```sh
yarn ios                        # run on iOS simulator
yarn start                      # start Metro
cd ios && pod install && cd -   # install pods
npx react-native run-ios --simulator="iPhone 15 Pro"
```

## 🗺 Roadmap (Milestones)
- M1: Auth + Onboarding + Tabs
- M2: Feed + Stories (view) + Post Detail
- M3: Post Composer + Upload Queue + Discover (grid)
- M4: Profiles + Follows + Likes + Comments
- M5: Clubs + Map + Notifications
- M6: Paywall + IAP + Premium gating
- M7: Moderation + Analytics + RC + Polishing/Accessibility

---

*Built with ❤️ for pet lovers everywhere*
