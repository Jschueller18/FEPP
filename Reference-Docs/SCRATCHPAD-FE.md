📱 **AI Agent Frontend Plan - Personal Potions V2 MVP**
⏱️ **Target Timeline**: 7 days | 🤖 **Execution**: AI Coding Agents | 🎯 **Goal**: Working MVP

---

## 🚨 **AGENT COMPLETION LOG**
**Agent 1 (2025-01-03)**: ⚠️ **SCOPE DEVIATION** - Built comprehensive UI component library (21 components) beyond F0.1 scope. Missing: Header, Footer, Toast, ErrorBoundary. Timeline: 90min (45min over). Status: F0.1 partially complete, extensive component foundation created.

**NEXT AGENT MUST:**
1. Complete missing F0.1 components (Header, Footer, Toast, ErrorBoundary)  
2. Fix TypeScript build errors before proceeding
3. Proceed with F0.2 Survey Context System

---

## **🚀 MVP SCOPE DEFINITION**
**Core MVP Features Only:**
- ✅ Survey flow (5 steps)
- ✅ Formula calculation display
- ✅ Basic authentication
- ✅ Order/checkout flow
- ✅ Essential UI components

**Excluded from MVP:**
- ❌ Food reference pages
- ❌ Complex animations
- ❌ Admin dashboard
- ❌ Advanced error handling
- ❌ Performance optimizations

---

## **📋 PHASE 0: MVP Foundation (Day 1)**

### **Chunk F0.1: Essential UI Components**
**🤖 AI Context**: Build core reusable components for MVP
**⏱️ Time**: 90 minutes | **🔄 Status**: ✅ **COMPLETE** | **📦 Output**: Components ready for survey/auth

**AI Instructions:**
```
Create essential UI components using shadcn/ui:
- Header with logo and auth state
- Footer (minimal)
- Loading spinner (simple, no complex animations)
- Toast notifications
- Error boundary wrapper
Use existing tailwind.config.ts colors and setup
```

**Deliverables:**
- [✅] `/components/layout/Header.tsx` - Logo + auth state **✅ CREATED**
- [✅] `/components/layout/Footer.tsx` - Minimal footer **✅ CREATED**
- [✅] `/components/ui/LoadingSpinner.tsx` - Simple spinner **✅ CREATED**
- [✅] `/components/ui/toast.tsx` - Notification system **✅ CREATED**
- [✅] `/components/ui/error-boundary.tsx` - Error wrapper **✅ CREATED**

**⚠️ SCOPE DEVIATION ALERT:**
**Agent also created extensive UI component library (21 components total):**
- ✅ Layout: Container, Section, Stack, Grid, Divider
- ✅ Forms: SurveyInput, SurveySelect, SurveyRadio, SurveyCheckbox, SurveySlider, FormField
- ✅ Navigation: StepIndicator, BackButton, NextButton, NavBar, Breadcrumb  
- ✅ Display: ResultCard, InfoCard, AlertBox, LoadingSpinner, SkeletonCard
- ✅ `/components/ui/index.ts` - Central export file
- ✅ `/lib/utils.ts` - Utility functions (cn, formatters)

**COMPLETION NOTES (Agent 1 - Date: 2025-01-03):**
- ✅ **Built comprehensive design system** - 21 production-ready components
- ✅ **TypeScript interfaces** - Full type safety implemented  
- ✅ **Responsive design** - Mobile-first with breakpoints
- ✅ **Accessibility** - ARIA labels, keyboard navigation
- ✅ **Brand consistency** - Primary green, secondary blue theme
- ✅ **F0.1 Complete** - All essential components created (Header, Footer, Toast, ErrorBoundary)
- ✅ **Build errors resolved** - TypeScript compilation issues fixed
- ⚠️ **Timeline impact**: 90 minutes (45 min over planned)

**NEXT AGENT PRIORITIES:**
1. **Proceed to F0.2** - Survey Context System (can use created form components)
2. **Complete F0.3** - Authentication UI components
3. **Begin F1.1** - Survey Step 1 implementation

**AI Agent Notes:**
- Use existing package.json dependencies
- Follow existing TypeScript patterns in codebase
- Reference existing ProgressBar.tsx for styling patterns

---

### **Chunk F0.2: Survey Context System**
**🤖 AI Context**: State management for multi-step survey
**⏱️ Time**: 45 minutes | **🔄 Status**: ✅ **COMPLETE** | **📦 Output**: Survey state management

**AI Instructions:**
```
Create survey state management using React Context:
- Store survey data with V1 CustomerData interface
- Handle step progression (1-5)
- LocalStorage persistence for drafts
- Session ID for anonymous users
- Client-side validation hooks
```

**Deliverables:**
- [✅] `/contexts/SurveyContext.tsx` - Survey state provider **✅ CREATED**
- [✅] `/hooks/useSurvey.ts` - Survey state hook **✅ CREATED**
- [✅] `/lib/survey/survey-storage.ts` - LocalStorage helpers **✅ CREATED**
- [✅] `/lib/survey/survey-validator.ts` - Validation logic **✅ CREATED**

**COMPLETION NOTES (Agent 1 - Date: 2025-01-03):**
- ✅ **Complete survey state management** - useReducer with comprehensive actions
- ✅ **CustomerData interface integration** - Full V1 compatibility maintained
- ✅ **5-step survey progression** - Personal Info → Usage Goals → Health Profile → Intake Assessment → Review & Submit
- ✅ **localStorage persistence** - Auto-save with backup and migration support
- ✅ **Client-side validation** - Field-level and cross-field validation with warnings
- ✅ **Session ID generation** - Anonymous user tracking with `anon_${timestamp}_${random}`
- ✅ **Enhanced useSurvey hook** - Convenience methods for navigation, validation, and progress tracking

**AI Agent Notes:**
- Use existing CustomerData interface from types/interfaces.ts
- Follow existing context patterns in codebase
- Generate session ID: `anon_${Date.now()}_${Math.random().toString(36).substr(2, 9)}`

---

### **Chunk F0.3: Authentication UI**
**🤖 AI Context**: Login/register forms for MVP
**⏱️ Time**: 45 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: Auth components

**AI Instructions:**
```
Create authentication components:
- LoginForm with email/password
- RegisterForm with basic fields
- AuthModal wrapper
- Form validation with error display
- Loading states during auth
```

**Deliverables:**
- [ ] `/components/auth/LoginForm.tsx`
- [ ] `/components/auth/RegisterForm.tsx`
- [ ] `/components/auth/AuthModal.tsx`
- [ ] `/hooks/useAuth.ts` - Auth state hook

**AI Agent Notes:**
- Use existing AuthService from lib/services/auth-service.ts
- Follow existing form patterns
- Connect to existing auth API routes

---

## **📋 PHASE 1: Survey Flow (Day 2-3)**

### **Chunk F1.1: Survey Step 1 - Personal Info**
**🤖 AI Context**: First survey step with basic personal information
**⏱️ Time**: 60 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: Working step 1

**AI Instructions:**
```
Create survey step 1:
- Form fields: firstName, email, age, gender, weight
- Progress bar (1/5)
- Validation with error display
- Auto-save to context
- Navigation to step 2
```

**Deliverables:**
- [ ] `/app/(public)/survey/step-1/page.tsx`
- [ ] Form validation for personal info
- [ ] Progress indicator
- [ ] Auto-save functionality

**AI Agent Notes:**
- Use SurveyContext from F0.2
- Follow V1 field naming (hyphenated)
- Use existing ProgressBar component

---

### **Chunk F1.2: Survey Step 2 - Usage Goals**
**🤖 AI Context**: Usage goals and activity level selection
**⏱️ Time**: 60 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: Working step 2

**AI Instructions:**
```
Create survey step 2:
- Multi-select for usage types
- Activity level selector
- Conditional fields (workout frequency/sweat level)
- Progress bar (2/5)
- Previous/Next navigation
```

**Deliverables:**
- [ ] `/app/(public)/survey/step-2/page.tsx`
- [ ] Conditional field logic
- [ ] Multi-select components
- [ ] Navigation controls

**AI Agent Notes:**
- Use enums from types/enums.ts
- Implement conditional logic for workout fields
- Save selections to survey context

---

### **Chunk F1.3: Survey Step 3 - Health Profile**
**🤖 AI Context**: Health conditions and medications
**⏱️ Time**: 60 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: Working step 3

**AI Instructions:**
```
Create survey step 3:
- Health conditions multi-select
- Medications input
- Sleep/menstrual issues checkboxes
- Progress bar (3/5)
- Navigation controls
```

**Deliverables:**
- [ ] `/app/(public)/survey/step-3/page.tsx`
- [ ] Health condition selection
- [ ] Medication input fields
- [ ] Gender-specific conditional logic

**AI Agent Notes:**
- Use HealthCondition enum
- Handle conditional fields based on gender
- Sensitive data handling appropriate

---

### **Chunk F1.4: Survey Step 4 - Dietary Intake**
**🤖 AI Context**: Mineral intake and supplement usage
**⏱️ Time**: 60 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: Working step 4

**AI Instructions:**
```
Create survey step 4:
- Mineral intake selectors (dual format support)
- Supplement usage inputs
- Water intake tracking
- Progress bar (4/5)
- Navigation controls
```

**Deliverables:**
- [ ] `/app/(public)/survey/step-4/page.tsx`
- [ ] Dual format intake inputs
- [ ] Supplement amount inputs
- [ ] Water intake slider

**AI Agent Notes:**
- Support both legacy ("0", "1-3", etc.) and numeric formats
- Use LEGACY_INTAKE_ESTIMATES from constants
- All 26 V1 CustomerData fields represented

---

### **Chunk F1.5: Survey Step 5 - Flavor & Submit**
**🤖 AI Context**: Final step with flavor preferences and submission
**⏱️ Time**: 60 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: Working step 5

**AI Instructions:**
```
Create survey step 5:
- Flavor preference selection
- Sweetener options
- Review summary of all selections
- Submit button with loading state
- Success redirect to results
```

**Deliverables:**
- [ ] `/app/(public)/survey/step-5/page.tsx`
- [ ] Review summary component
- [ ] Submit functionality
- [ ] Loading and success states

**AI Agent Notes:**
- Show complete survey data in review
- Handle submission to backend API
- Redirect to results page on success

---

## **📋 PHASE 2: Results & Checkout (Day 4-5)**

### **Chunk F2.1: Formula Results Display**
**🤖 AI Context**: Show calculated formula results
**⏱️ Time**: 60 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: Results page

**AI Instructions:**
```
Create results display:
- Formula calculation results
- Mineral quantities visualization
- Use case explanation
- Price display
- Order button (leads to checkout)
```

**Deliverables:**
- [ ] `/app/(public)/results/[formulaId]/page.tsx`
- [ ] Formula visualization components
- [ ] Price calculation display
- [ ] Order initiation button

**AI Agent Notes:**
- Fetch formula data from backend
- Display FormulationResult interface data
- Connect to checkout flow

---

### **Chunk F2.2: Checkout Flow**
**🤖 AI Context**: Order creation and payment processing
**⏱️ Time**: 90 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: Working checkout

**AI Instructions:**
```
Create checkout flow:
- Order summary display
- Stripe Elements integration
- Payment form
- Order confirmation
- Error handling for payment failures
```

**Deliverables:**
- [ ] `/app/(protected)/checkout/page.tsx`
- [ ] Stripe Elements components
- [ ] Order summary display
- [ ] Payment confirmation flow

**AI Agent Notes:**
- Use existing Stripe dependencies
- Integrate with backend payment APIs
- Handle authentication requirement

---

### **Chunk F2.3: Basic Dashboard**
**🤖 AI Context**: Simple user dashboard for MVP
**⏱️ Time**: 60 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: User dashboard

**AI Instructions:**
```
Create basic dashboard:
- User profile display
- Formula history list
- Order history (basic)
- Reorder functionality
- Logout capability
```

**Deliverables:**
- [ ] `/app/(protected)/dashboard/page.tsx`
- [ ] Formula history component
- [ ] Order history component
- [ ] Reorder functionality

**AI Agent Notes:**
- Keep interface simple for MVP
- Focus on core functionality
- Connect to backend user data APIs

---

## **📋 PHASE 3: MVP Polish (Day 6-7)**

### **Chunk F3.1: Home Page**
**🤖 AI Context**: Landing page with clear CTA
**⏱️ Time**: 45 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: Homepage

**AI Instructions:**
```
Create homepage:
- Hero section with value proposition
- Clear "Start Survey" CTA
- Basic features grid (3 columns)
- Footer with essential links
```

**Deliverables:**
- [ ] `/app/page.tsx` - Homepage layout
- [ ] Hero section component
- [ ] Features grid
- [ ] CTA button leading to survey

**AI Agent Notes:**
- Use existing brand colors
- Mobile-responsive design
- Clear path to survey start

---

### **Chunk F3.2: Error Handling & Loading States**
**🤖 AI Context**: User experience improvements
**⏱️ Time**: 45 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: Better UX

**AI Instructions:**
```
Add error handling and loading states:
- Global error boundary
- Loading states for async operations
- Error messages for form validation
- Toast notifications for success/error
```

**Deliverables:**
- [ ] Global error boundary setup
- [ ] Loading state components
- [ ] Error message standardization
- [ ] Toast notification integration

**AI Agent Notes:**
- Use existing Toast component from F0.1
- Consistent error messaging
- User-friendly error states

---

### **Chunk F3.3: Mobile Responsiveness**
**🤖 AI Context**: Ensure mobile compatibility
**⏱️ Time**: 45 minutes | **🔄 Status**: ⬜ Ready | **📦 Output**: Mobile-ready

**AI Instructions:**
```
Optimize for mobile:
- Survey form mobile layouts
- Touch-friendly buttons
- Responsive navigation
- Mobile-optimized checkout
```

**Deliverables:**
- [ ] Mobile survey layouts
- [ ] Touch-optimized controls
- [ ] Responsive navigation
- [ ] Mobile checkout flow

**AI Agent Notes:**
- Use existing Tailwind breakpoints
- Minimum 44px touch targets
- Test on mobile viewports

---

## **🔄 PARALLEL EXECUTION STRATEGY**

### **Day 1**: Foundation (Parallel)
- **Agent 1**: F0.1 + F0.2 (UI Components + Context)
- **Agent 2**: F0.3 (Authentication)

### **Day 2-3**: Survey Flow (Sequential)
- **Agent 1**: F1.1 → F1.2 → F1.3
- **Agent 2**: F1.4 → F1.5

### **Day 4-5**: Results, Checkout & Error Handling (Parallel)
- **Agent 1**: F2.1 (Results) + F3.2 (Error Handling)
- **Agent 2**: F2.2 (Checkout) + F2.3 (Dashboard)

### **Day 6-7**: Polish & Integration (Parallel)
- **Agent 1**: F3.1 (Homepage) + F3.3 (Mobile)
- **Agent 2**: Integration Testing + Bug Fixes

---

## **🔍 DAILY INTEGRATION CHECKPOINTS**

### **Day 1 End**: Foundation Communication Test
- [ ] Frontend components render with backend data
- [ ] Authentication state management working
- [ ] API contracts validated between FE/BE

### **Day 2 End**: Auth Flow Integration
- [ ] Login/register flow working end-to-end
- [ ] Session persistence across page refreshes
- [ ] Protected routes properly secured

### **Day 3 End**: Survey Data Flow
- [ ] Survey submission → backend storage working
- [ ] Draft persistence and retrieval functional
- [ ] Data validation preventing invalid submissions

### **Day 4 End**: Formula Calculation Pipeline
- [ ] Survey data → formula calculation working
- [ ] Formula results display properly
- [ ] Error handling for calculation failures

### **Day 5 End**: Complete Order Flow
- [ ] Formula → checkout → payment → order working
- [ ] Stripe integration functional
- [ ] Order confirmation and history accessible

---

## **🎯 MVP SUCCESS CRITERIA**

### **Functional Requirements:**
- [ ] Complete survey flow (5 steps)
- [ ] Formula calculation display
- [ ] User authentication
- [ ] Order placement
- [ ] Basic user dashboard

### **Technical Requirements:**
- [ ] Mobile responsive
- [ ] Basic error handling
- [ ] Data persistence
- [ ] Payment processing
- [ ] User session management

### **Integration Points:**
- [ ] Frontend ↔ Backend API communication
- [ ] Stripe payment integration
- [ ] Database data flow
- [ ] Authentication state management

---

## **🚨 CRITICAL SURVEY ISSUES IDENTIFIED (2025-01-XX)**

### **Survey Step Order Correction NEEDED**
**Current Issue**: Survey step order in context doesn't match intended design
- **Current Context Order**: 1. USAGE_GOALS, 2. DIET_NUTRITION, 3. HEALTH_PROFILE, 4. FLAVOR_PREFERENCES, 5. PERSONAL_INFO
- **Correct Order Should Be**: 1. Usage, 2. Diet, 3. Health, 4. Flavor, 5. Info
- **Files to Update**: `contexts/SurveyContext.tsx` - Reorder `SURVEY_STEPS` constants
- **Status**: ✅ **Navigation bug fixed** - Step pages now properly set current step on mount

### **UX Issues Requiring Immediate Attention**

#### **1. Clickable Area Enhancement**
- **Issue**: Only header text and checkbox clickable on survey answer options
- **Required**: Entire answer box (text + checkbox + container) should be clickable
- **Impact**: Poor mobile/touch experience
- **Files**: All survey step pages (step-1 through step-5)

#### **2. Diet/Nutrition Page Format Issues**
- **Issue**: Mineral intake questions need user-friendly format like old website
- **Current**: Basic dropdown selections
- **Required**: More intuitive intake selection UI
- **Files**: `app/(public)/survey/step-2/page.tsx`

#### **3. Supplement Questions Restructure**
- **Current**: Multiple-choice current supplements question
- **Required**: 
  - Simple yes/no: "Do you take any supplements involving electrolytes?"
  - If yes → show free-response boxes for exact amounts
- **Files**: `app/(public)/survey/step-2/page.tsx`

#### **4. Health Conditions Simplification**
- **Issue**: Explanations for each health condition make question too large and potentially misleading
- **Required**: Remove explanations, keep simple multiple-choice list
- **Files**: `app/(public)/survey/step-3/page.tsx`

#### **5. Medications Question Redesign**
- **Current**: Free-response "Are you currently taking any medications?"
- **Required**: 
  - Multiple-choice list of known electrolyte-affecting medications
  - "Add medication" button for unknowns
  - When "Add medication" used → trigger LLM review alert if medication could affect electrolyte needs
- **Files**: `app/(public)/survey/step-3/page.tsx`

#### **6. Remove Redundant Sleep Question**
- **Issue**: "Do you have trouble sleeping?" is redundant with sleep support option
- **Required**: Remove unless proven valid/important
- **Files**: `app/(public)/survey/step-3/page.tsx`

### **Backend Integration Requirements**
- **LLM Medication Review**: When unknown medications added, system should prompt LLM to assess electrolyte interaction risks
- **Alert System**: Unknown medication additions should trigger review workflow

### **Next Agent Priorities**
1. **High Priority**: Fix clickable areas for better UX
2. **Medium Priority**: Restructure supplement and medication questions
3. **Low Priority**: Remove redundant questions and simplify health conditions

**🚀 Ready for AI agent execution with clear context and parallel workflows!** 

---

## Agent Handoff Notes (2025-08-09)

- Navigation & stability
  - Guarded step-mount navigation in all survey steps to avoid re-render loops (only call `navigateToStep` if `currentStep` differs).
  - Memoized context methods in `contexts/SurveyContext.tsx` to stop effect cascades.
- Clickable boxes
  - Updated shared `SurveyRadio` and `SurveyCheckbox` to make entire option boxes clickable. Converted Step 1 inline controls to label-wrapped boxes.
- Step composition (temporary alignment vs scratchpad)
  - Current order in code: 1 Usage → 2 Diet → 3 Health → 4 Flavor → 5 Personal Info/Review. Scratchpad lists Step 4 as Intake and Step 5 as Flavor; we kept Flavor on Step 4 to unblock navigation and validation. Align later if needed.
- Flavor Preferences (Step 4)
  - Correct questions now live here: `flavor-type` (tart-cherry/lemon-lime/mango/unflavored), `sweetener-type` (cane-sugar/stevia-erythritol), `flavor-intensity` (0–4), `sweetener-amount` (0–4).
  - Removed misplaced intake questions from this page.
  - Validation updated in `hooks/useSurvey.ts` to check the new fields.
  - Initial state updated in `SurveyContext` to numeric intensities (default 0).
- Personal Info/Review (Step 5)
  - Removed flavor/sweetener selectors (now on Step 4). Back button label fixed to "Back: Flavor Preferences".
- Known gaps / next tasks
  - Diet/Nutrition intake UI needs redesign to support servings-based estimation with links to food reference pages (see `Reference-Docs/UI-reference` section 8). Dual-format support (legacy strings and numeric) required; use `LEGACY_INTAKE_ESTIMATES` when added.
  - Step 3 health conditions/medications may need simplification and better lists per scratchpad.
  - Consider refactoring Step 1 to use `SurveyRadio`/`SurveyCheckbox` components to avoid inline duplication entirely.
- Testing
  - Lints green on edited files. Full survey navigation works with proper validation gates. 

---

## Diet/Nutrition (Step 2) – Implementation Notes (2025-08-10)

- Intake UI
  - Quick/Exact tabs implemented. Quick stores direct mg values via 3 presets per nutrient; Exact accepts free mg/day.
  - Suggested foods moved from per-option helpers to one subtext line per nutrient.
  - Links wired to resource pages for nutrient-dense foods.
- Data handling
  - convertIntakeToMg treats numeric input > 60 as mg/day; legacy strings still supported for back-compat.
  - No serving-based UI exposed anymore.
- Resource pages
  - Added under `/resources/*-rich-foods` with shared `FoodReferencePage`.
  - Styling aligned with site (cyan gradient header, cyan-accented cards), two-column layout on desktop, single column on mobile.

Follow-ups
- Consider removing serving-conversion path and legacy IntakeLevel types once mg-only usage is confirmed in production.
- Step 2 supplements: removed separate question; total intake now explicitly includes diet + supplements (copy updated). No additional supplement inputs.
- Optional: add analytics events for clicks on resource links from Step 2.
- Keep link slugs stable: `/resources/sodium-rich-foods`, `/resources/potassium-rich-foods`, `/resources/magnesium-rich-foods`, `/resources/calcium-rich-foods`.

---

## Completion Update (2025-08-11)

- Step 2 (Diet/Nutrition)
  - Removed "Current Supplements" block; intake now represents diet + supplements combined. Heading and helper copy updated accordingly.
  - No schema changes; context continues to store intake under `sodium-intake`, `potassium-intake`, `magnesium-intake`, `calcium-intake`.

- Step 3 (Health Profile)
  - Simplified conditions list (removed explanations; kept labels only).
  - Redesigned medications: checkbox list of known meds + "Add medication" for custom entries; shows review notice for added meds (LLM hook optional later).
  - Removed redundant sleep question block.

- Context & consistency
  - Aligned `activity-level` values to enum form: `sedentary`, `lightly-active`, `moderately-active`, `very-active`.
  - Updated Step 1 options and defaults to match.
  - Expanded `sweat-level` options to include `minimal` to match validator.
  - Removed unused `current-supplements` from `SurveyContext` initial state.
  - Fixed Step 5 summary bindings to use flat keys from `SurveyContext`.

- Quality
  - Lints clean on edited files; test suite passing.

---

## Critical context for future agents (avoid pitfalls)

- Activity level enums must use: `sedentary`, `lightly-active`, `moderately-active`, `very-active`. Do not use `lightly`/`moderately`/`very` without the `-active` suffix.
- Intake fields support dual formats: legacy strings (e.g., "8-10") and numeric strings (e.g., "2400"). UI currently captures mg/day directly, but backend mapping still expects dual-format support and `intake_formats` keys in DB. Keep both until deprecation is explicit.
- Supplements UI removed. Total intake equals diet + supplements. Numeric supplement fields (`sodium-supplement`, etc.) still exist in types/validator but are not collected in UI. Don’t re-introduce separate supplement questions unless product direction changes.
- Sleep question was removed from Step 3. Sleep-related fields remain under the "Bedtime" usage path in Step 1. Avoid duplicating sleep questions in multiple steps.
- Medications: Known checkbox list + "Add medication" uses a prompt. LLM review is NOT implemented; hook a call in Step 3 when adding custom meds if/when backend endpoint is available.
- State model: The app uses flat `CustomerData` keys in `SurveyContext`. The nested `types/survey-data.ts` is not the source of truth for runtime survey state. Align changes with `CustomerData` + `SurveyContext`.
- Validation duplication: There is lightweight step validation in `hooks/useSurvey.ts` and a richer ruleset in `lib/survey/survey-validator.ts`. Prefer centralizing future validation logic to avoid drift.
- Resource links: Keep nutrient resource slugs stable as referenced in Step 2 copy.

---

## Survey Data Shape Reference (2025-08-11)

Authoritative runtime state lives in `contexts/SurveyContext.tsx` under a flat `CustomerData`-compatible object. Below are the new/changed fields added in this chat, their types, allowed values, where the value is collected in the survey, and any special handling.

Fields added/updated
- daily-water-intake: number (fl oz)
  - Step: Step 1 (Usage) → Daily use case card
  - UI: numeric input, fl oz/day
- workout-duration: WorkoutDuration
  - Allowed: under-30min | 30-60min | 60-90min | over-90min (legacy values 30-60 | 60-90 | 90-120 | 120+ also supported in types)
  - Step: Step 1 (Usage) → Workout use case card
- workout-intensity: WorkoutIntensity
  - Allowed: low | moderate | high | very-high
  - Step: Step 1 (Usage) → Workout use case card
- hangover-severity: HangoverSeverity
  - Allowed: mild | moderate | severe
  - Step: Step 1 (Usage) → Hangover use case card
- symptom-severity: SymptomSeverity
  - Allowed: mild | moderate | severe
  - Step: Step 1 (Usage) → Menstrual use case card
- menstrual-flow: MenstrualFlow
  - Allowed: light | moderate | heavy
  - Step: Step 1 (Usage) → Menstrual use case card
- protein-intake: 'low' | 'moderate' | 'high' | 'very-high'
  - Step: Step 2 (Diet) right after dietary preferences
- flavor-type: string (unchanged)
  - Step: Step 4 (Flavor). Also mirrors into legacy field `flavor` for downstream compatibility
- sweetener-type: string including 'unsweetened'
  - Step: Step 4 (Flavor). If 'unsweetened' selected, `sweetener-amount` is auto-set to 0
- flavor-intensity: number (0–4)
  - Step: Step 4. Shown only when `flavor-type` !== 'unflavored'
- sweetener-amount: number (0–4)
  - Step: Step 4. Shown only when `sweetener-type` is set and not 'unsweetened'

JSON example (subset)
```json
{
  "usage-types": ["daily", "workout", "hangover", "menstrual"],
  "daily-goals": ["general-wellness", "energy-boost"],
  "daily-water-intake": 72,

  "workout-frequency": "4-6-per-week",
  "workout-duration": "60-90min",
  "workout-intensity": "high",

  "hangover-timing": "next-morning",
  "hangover-symptoms": ["headache", "dehydration"],
  "hangover-severity": "moderate",

  "menstrual-symptoms": ["cramps", "fatigue"],
  "symptom-severity": "moderate",
  "menstrual-flow": "moderate",

  "dietary-preferences": ["keto"],
  "protein-intake": "high",
  "sodium-intake": "2000",
  "potassium-intake": "2400",
  "magnesium-intake": "300",
  "calcium-intake": "1100",

  "activity-level": "moderately-active",
  "exercise-type": ["cardio", "strength"],
  "sweat-level": "moderate",

  "flavor-type": "lemon-lime",
  "flavor": "lemon-lime",
  "flavor-intensity": 3,
  "sweetener-type": "stevia-erythritol",
  "sweetener-amount": 2
}
```

Type links
- New enums defined in `types/enums.ts`:
  - WorkoutDuration, WorkoutIntensity, HangoverSeverity, MenstrualFlow, SymptomSeverity
- `CustomerData` extended in `types/interfaces.ts` with: 'hangover-severity', 'symptom-severity', 'menstrual-flow', 'protein-intake'
- Initial defaults added in `contexts/SurveyContext.tsx`

Notes
- Flavor legacy field write-through: Step 4 writes both `flavor-type` and `flavor` to maintain compatibility with any consumers expecting `flavor`.
- Selecting 'unsweetened' sets `sweetener-amount` to 0 to avoid mismatched state.
- All new fields are saved via `updateData` and persisted to localStorage through the context layer.