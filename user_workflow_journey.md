# UX Design User Workflow Documentation: Youth Account Fund Management

## Experience Mindset

**Primary User:** Parent/Guardian
**Experience:** Managing and teaching financial responsibility for a youth account

### Key Experiences & Scenarios

1. **Accessing Youth Account Dashboard**
   - Scenario 1A: Parent logs in and views youth account dashboard (standard)
   - Scenario 1B: Parent logs in, but youth account is not yet set up (edge)
2. **Allocating Funds to Youth Account**
   - Scenario 2A: Parent transfers funds successfully
   - Scenario 2B: Parent attempts transfer with insufficient balance (error)
   - Scenario 2C: Parent enters invalid transfer amount (edge)
3. **Setting Spending Limits**
   - Scenario 3A: Parent sets or updates weekly spending limit
   - Scenario 3B: Parent attempts to set invalid limit (edge)
4. **Viewing Youth Spending Activity**
   - Scenario 4A: Parent reviews recent youth transactions
   - Scenario 4B: Parent filters activity by date/merchant (variation)
5. **Spending Limit Enforcement**
   - Scenario 5A: Youth attempts transaction exceeding limit; parent notified
   - Scenario 5B: Parent reviews blocked transaction (edge)
6. **Concurrent Access**
   - Scenario 6A: Parent and youth access account simultaneously (edge)

---

## Scenario 1: Accessing Youth Account Dashboard

### Scenario 1A: Standard Dashboard Access
- **Context:** Parent is logged in and has a youth account linked
- **Action:** Navigates to youth account section
- **Goal:** Quickly view balance and recent activity
- **User Goal:** Instantly see youth account status and activity
- **Business Goal:** Increase engagement and trust by providing transparency

#### Workflow Variation 1
- 1.0 Login Screen
- 2.0 Main Dashboard (with youth account summary)
- 3.0 Youth Account Dashboard (detailed view)

#### Workflow Variation 2
- 1.0 Login Screen
- 2.0 Accounts Overview (list of all accounts)
- 3.0 Select Youth Account
- 4.0 Youth Account Dashboard

##### Screen Details

**1.0 Login Screen**
- Goal: Secure authentication
- Description: Parent enters credentials
- Design Problem: HMW make login frictionless but secure?
- Design Opportunity: What if biometric login is offered?

**2.0 Main Dashboard / Accounts Overview**
- Goal: Overview of all accounts
- Description: Parent sees balances for all linked accounts
- Design Problem: HMW highlight youth account for quick access?
- Design Opportunity: What if youth account is pinned or color-coded?

**3.0/4.0 Youth Account Dashboard**
- Goal: Show youth account balance, recent activity, quick actions
- Description: Balance, recent transactions, Add Funds, Set Limit
- Design Problem: HMW surface key actions without clutter?
- Design Opportunity: What if dashboard is customizable?

##### Sequence
- Variation 1: 1.0 Login -> 2.0 Main Dashboard -> 3.0 Youth Account Dashboard
- Variation 2: 1.0 Login -> 2.0 Accounts Overview -> 3.0 Select Youth Account -> 4.0 Youth Account Dashboard

---

### Scenario 1B: Youth Account Not Set Up (Edge)
- **Context:** Parent logs in, no youth account exists
- **Action:** Navigates to youth account section
- **Goal:** Prompt setup
- **User Goal:** Easily set up youth account
- **Business Goal:** Drive adoption of youth accounts

#### Workflow Variation 1
- 1.0 Login Screen
- 2.0 Main Dashboard
- 3.0 Youth Account Setup Prompt

#### Workflow Variation 2
- 1.0 Login Screen
- 2.0 Accounts Overview
- 3.0 Add New Account -> Youth Account Setup

##### Screen Details

**3.0 Youth Account Setup Prompt**
- Goal: Encourage setup
- Description: Benefits, quick start, required info
- Design Problem: HMW reduce friction in onboarding?
- Design Opportunity: What if setup is gamified?

##### Sequence
- Variation 1: 1.0 Login -> 2.0 Main Dashboard -> 3.0 Youth Account Setup Prompt
- Variation 2: 1.0 Login -> 2.0 Accounts Overview -> 3.0 Add New Account -> 4.0 Youth Account Setup

---

## Scenario 2: Allocating Funds to Youth Account

### Scenario 2A: Successful Fund Transfer
- **Context:** Parent wants to add funds
- **Action:** Selects "Add Funds", enters amount, confirms
- **Goal:** Transfer funds quickly and securely
- **User Goal:** Move money to youth account with confidence
- **Business Goal:** Encourage regular funding, reduce errors

#### Workflow Variation 1
- 1.0 Youth Account Dashboard
- 2.0 Add Funds Pop-Up (Pu.1)
- 3.0 Transfer Confirmation (Pu.2)
- 4.0 Success Message (Pu.3)

#### Workflow Variation 2
- 1.0 Youth Account Dashboard
- 2.0 Add Funds Full Page
- 3.0 Review & Confirm
- 4.0 Success Page

##### Screen Details

**Pu.1 Add Funds Pop-Up**
- Goal: Enter transfer details
- Description: Source account, amount, validation
- Design Problem: HMW prevent invalid entries?
- Design Opportunity: What if smart suggestions for amounts?

**Pu.2 Transfer Confirmation**
- Goal: Prevent accidental transfers
- Description: Review details, confirm/cancel
- Design Problem: HMW reduce cognitive load?
- Design Opportunity: What if confirmation uses plain language?

**Pu.3 Success Message**
- Goal: Reassure parent
- Description: Transfer complete, new balance
- Design Problem: HMW reinforce positive action?
- Design Opportunity: What if offer to set recurring transfer?

##### Sequence
- Variation 1: 1.0 Dashboard -> Pu.1 Add Funds -> Pu.2 Confirm -> Pu.3 Success
- Variation 2: 1.0 Dashboard -> 2.0 Add Funds Page -> 3.0 Review -> 4.0 Success

---

### Scenario 2B: Insufficient Balance (Error)
- **Context:** Parent tries to transfer more than available
- **Action:** System blocks transfer
- **Goal:** Prevent overdraft, inform user
- **User Goal:** Understand why transfer failed
- **Business Goal:** Reduce support calls, build trust

#### Workflow Variation 1
- 1.0 Add Funds Pop-Up
- Er.1 Insufficient Funds Error

#### Workflow Variation 2
- 1.0 Add Funds Page
- Er.2 Inline Error Message

##### Screen Details

**Er.1/Er.2 Insufficient Funds Error**
- Goal: Clearly communicate issue
- Description: Error message, guidance to resolve
- Design Problem: HMW avoid frustration?
- Design Opportunity: What if suggest lower amount or link to help?

##### Sequence
- Variation 1: 1.0 Add Funds Pop-Up -> Er.1 Error
- Variation 2: 1.0 Add Funds Page -> Er.2 Inline Error

---

### Scenario 2C: Invalid Transfer Amount (Edge)
- **Context:** Parent enters negative, zero, or non-numeric amount
- **Action:** System validates and blocks
- **Goal:** Prevent invalid transactions
- **User Goal:** Correct mistakes easily
- **Business Goal:** Reduce transaction errors

#### Workflow Variation 1
- 1.0 Add Funds Pop-Up
- Er.3 Validation Error

#### Workflow Variation 2
- 1.0 Add Funds Page
- Er.4 Inline Validation

##### Screen Details

**Er.3/Er.4 Validation Error**
- Goal: Guide user to valid input
- Description: Real-time feedback
- Design Problem: HMW make errors non-blocking?
- Design Opportunity: What if show valid range dynamically?

##### Sequence
- Variation 1: 1.0 Add Funds Pop-Up -> Er.3 Error
- Variation 2: 1.0 Add Funds Page -> Er.4 Inline Error

---

## Scenario 3: Setting Spending Limits

### Scenario 3A: Set/Update Weekly Limit
- **Context:** Parent wants to control youth spending
- **Action:** Configures weekly limit
- **Goal:** Set clear boundaries
- **User Goal:** Easily set and adjust limits
- **Business Goal:** Promote responsible spending

#### Workflow Variation 1
- 1.0 Youth Account Dashboard
- 2.0 Set Limit Pop-Up (Pu.4)
- 3.0 Confirmation (Pu.5)

#### Workflow Variation 2
- 1.0 Youth Account Dashboard
- 2.0 Spending Limit Page
- 3.0 Save & Confirm

##### Screen Details

**Pu.4 Set Limit Pop-Up / Spending Limit Page**
- Goal: Input and explain limits
- Description: Input field, info tooltip, current limit display
- Design Problem: HMW explain impact of limits?
- Design Opportunity: What if show projected savings?

**Pu.5 Confirmation**
- Goal: Confirm change
- Description: Success message, updated dashboard
- Design Problem: HMW reinforce positive behavior?
- Design Opportunity: What if offer to notify youth?

##### Sequence
- Variation 1: 1.0 Dashboard -> Pu.4 Set Limit -> Pu.5 Confirm
- Variation 2: 1.0 Dashboard -> 2.0 Limit Page -> 3.0 Save & Confirm

---

### Scenario 3B: Invalid Limit (Edge)
- **Context:** Parent enters negative or excessively high limit
- **Action:** System blocks and explains
- **Goal:** Prevent unrealistic limits
- **User Goal:** Understand valid range
- **Business Goal:** Maintain system integrity

#### Workflow Variation 1
- 1.0 Set Limit Pop-Up
- Er.5 Invalid Limit Error

#### Workflow Variation 2
- 1.0 Spending Limit Page
- Er.6 Inline Validation

##### Screen Details

**Er.5/Er.6 Invalid Limit Error**
- Goal: Guide to valid input
- Description: Error message, valid range
- Design Problem: HMW prevent frustration?
- Design Opportunity: What if suggest typical limits?

##### Sequence
- Variation 1: 1.0 Set Limit Pop-Up -> Er.5 Error
- Variation 2: 1.0 Limit Page -> Er.6 Inline Error

---

## Scenario 4: Viewing Youth Spending Activity

### Scenario 4A: Review Transactions
- **Context:** Parent wants to monitor spending
- **Action:** Views activity section
- **Goal:** Quickly scan transactions
- **User Goal:** Spot trends, identify issues
- **Business Goal:** Build trust, reduce disputes

#### Workflow Variation 1
- 1.0 Youth Account Dashboard
- 2.0 Activity Tab/List

#### Workflow Variation 2
- 1.0 Youth Account Dashboard
- 2.0 Activity Page with Filters

##### Screen Details

**2.0 Activity Tab/List/Page**
- Goal: Present clear, scannable data
- Description: Date, merchant, amount, balance, filters
- Design Problem: HMW make patterns visible?
- Design Opportunity: What if offer visualizations or alerts?

##### Sequence
- Variation 1: 1.0 Dashboard -> 2.0 Activity Tab
- Variation 2: 1.0 Dashboard -> 2.0 Activity Page (with filters)

---

### Scenario 4B: Filter Activity (Variation)
- **Context:** Parent filters by date, merchant, or amount
- **Action:** Uses filter controls
- **Goal:** Find specific transactions
- **User Goal:** Investigate spending
- **Business Goal:** Reduce support queries

#### Workflow Variation 1
- 1.0 Activity Page
- 2.0 Filter Pop-Up (Pu.6)

#### Workflow Variation 2
- 1.0 Activity Page
- 2.0 Inline Filter Controls

##### Screen Details

**Pu.6 Filter Pop-Up / Inline Controls**
- Goal: Refine transaction list
- Description: Date picker, merchant dropdown, amount range
- Design Problem: HMW keep filtering simple?
- Design Opportunity: What if save frequent filters?

##### Sequence
- Variation 1: 1.0 Activity Page -> Pu.6 Filter
- Variation 2: 1.0 Activity Page -> 2.0 Inline Filter

---

## Scenario 5: Spending Limit Enforcement

### Scenario 5A: Youth Exceeds Limit (Edge)
- **Context:** Youth tries to spend over limit
- **Action:** Transaction blocked, parent notified
- **Goal:** Enforce rules, inform stakeholders
- **User Goal:** Parent stays in control
- **Business Goal:** Prevent overspending, build trust

#### Workflow Variation 1
- 1.0 System blocks transaction
- Em.1 Parent receives email notification

#### Workflow Variation 2
- 1.0 System blocks transaction
- Pu.7 In-app notification for parent

##### Screen Details

**Em.1 Email Notification / Pu.7 In-app Notification**
- Goal: Alert parent
- Description: Transaction details, next steps
- Design Problem: HMW avoid notification fatigue?
- Design Opportunity: What if allow notification preferences?

##### Sequence
- Variation 1: 1.0 Blocked Transaction -> Em.1 Email
- Variation 2: 1.0 Blocked Transaction -> Pu.7 In-app Notification

---

## Scenario 6: Concurrent Access (Edge)
- **Context:** Parent and youth access account at same time
- **Action:** Both perform actions
- **Goal:** Ensure data consistency
- **User Goal:** No confusion or errors
- **Business Goal:** Maintain integrity, prevent race conditions

#### Workflow Variation 1
- 1.0 Parent Dashboard
- 2.0 Youth Transaction
- 3.0 Real-time balance update

#### Workflow Variation 2
- 1.0 Parent Dashboard
- 2.0 Youth Transaction
- 3.0 Conflict Resolution Pop-Up (Pu.8) if needed

##### Screen Details

**Pu.8 Conflict Resolution Pop-Up**
- Goal: Resolve simultaneous actions
- Description: Explain conflict, suggest retry
- Design Problem: HMW minimize disruption?
- Design Opportunity: What if show real-time sync status?

##### Sequence
- Variation 1: 1.0 Parent Dashboard -> 2.0 Youth Transaction -> 3.0 Real-time Update
- Variation 2: 1.0 Parent Dashboard -> 2.0 Youth Transaction -> Pu.8 Conflict Pop-Up

---

# Summary Table of All Screens

| Screen/State         | Goal                                      | Description/Features                                                                 | Design Problems                                    | Design Opportunities                              |
|---------------------|-------------------------------------------|-------------------------------------------------------------------------------------|----------------------------------------------------|---------------------------------------------------|
| 1.0 Login           | Secure authentication                     | Credential input, error handling, biometric option                                   | Friction vs. security                              | Biometric, passwordless login                     |
| 2.0 Main Dashboard  | Overview of all accounts                  | Balances, quick links, highlight youth account                                       | Highlighting, info overload                        | Pinning, color-coding                             |
| 3.0 Youth Dashboard | Show youth account status & actions       | Balance, activity, Add Funds, Set Limit, quick actions                              | Info hierarchy, action prominence                  | Customizable dashboard                            |
| Pu.1 Add Funds      | Enter transfer details                    | Source, amount, validation, suggestions                                             | Preventing errors                                 | Smart suggestions                                 |
| Pu.2 Confirm        | Prevent accidental transfer               | Review, confirm/cancel                                                              | Cognitive load                                    | Plain language confirmation                       |
| Pu.3 Success        | Reassure parent                           | Success message, new balance, next steps                                            | Reinforcing action                                | Offer recurring transfer                          |
| Er.1/Er.2 Error     | Communicate insufficient funds            | Error message, guidance                                                             | Avoiding frustration                              | Suggest lower amount, help link                   |
| Pu.4 Set Limit      | Input and explain limits                  | Input, info tooltip, current limit                                                  | Explaining impact                                 | Projected savings                                 |
| Pu.5 Confirm        | Confirm limit change                      | Success message, updated dashboard                                                  | Reinforcing behavior                              | Notify youth                                      |
| 2.0 Activity        | Present clear, scannable data             | Date, merchant, amount, balance, filters                                            | Making patterns visible                           | Visualizations, alerts                            |
| Pu.6 Filter         | Refine transaction list                   | Date picker, merchant dropdown, amount range                                        | Keeping filtering simple                           | Save frequent filters                             |
| Em.1 Notification   | Alert parent                              | Transaction details, next steps                                                     | Notification fatigue                              | Notification preferences                          |
| Pu.8 Conflict       | Resolve simultaneous actions              | Explain conflict, suggest retry                                                     | Minimizing disruption                             | Real-time sync status                             |

---

# Accessibility & Scalability Considerations
- All screens must be WCAG 2.1 AA compliant (color contrast, keyboard navigation, screen reader labels)
- Responsive layouts for desktop, tablet, and mobile
- Error messages must be clear, actionable, and accessible
- All actions must be undoable or confirmable to prevent accidental changes
- Notification preferences for accessibility (email, SMS, in-app)
- Scalable design system for future features (multiple youth accounts, advanced analytics)

---

# Complete Workflow Sequences (Examples)

## Fund Transfer (Standard)
1.0 Login -> 2.0 Main Dashboard -> 3.0 Youth Dashboard -> Pu.1 Add Funds -> Pu.2 Confirm -> Pu.3 Success

## Set Spending Limit (Standard)
1.0 Login -> 2.0 Main Dashboard -> 3.0 Youth Dashboard -> Pu.4 Set Limit -> Pu.5 Confirm

## View Activity (With Filters)
1.0 Login -> 2.0 Main Dashboard -> 3.0 Youth Dashboard -> 2.0 Activity -> Pu.6 Filter

## Error: Insufficient Funds
1.0 Login -> 2.0 Main Dashboard -> 3.0 Youth Dashboard -> Pu.1 Add Funds -> Er.1 Error

## Edge: Concurrent Access
1.0 Parent Dashboard -> 2.0 Youth Transaction -> Pu.8 Conflict Pop-Up

---

# End of UX Design User Workflow Documentation
