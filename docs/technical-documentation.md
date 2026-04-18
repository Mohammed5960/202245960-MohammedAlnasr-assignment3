# Technical Documentation

## 1. Project Structure

- `index.html`: main layout and structure
- `css/styles.css`: styling, responsiveness, and transitions
- `js/script.js`: all JavaScript logic
- `docs/`: documentation files

---

## 2. GitHub API Integration

The application fetches repositories using:
https://api.github.com/users/{username}/repos

### Implementation Steps:
1. Use `fetch()` to request data
2. Check if response is successful
3. Convert response to JSON
4. Loop through repositories
5. Create HTML elements dynamically
6. Append them to the page

### Error Handling:
- If API fails → show error message
- If no repositories → show empty state message
- While loading → show "Loading..." message

---

## 3. Project Filtering and Sorting

### Filtering:
- Based on category selected by user
- Compares selected category with project data

### Searching:
- Converts user input to lowercase
- Matches against project title and description

### Sorting:
- A-Z / Z-A → uses `localeCompare()`
- Newest / Oldest → compares project year

### Combined Logic:
- First filter → then search → then sort
- Final results are rendered dynamically

---

## 4. State Management

### Dark Mode:
- Stored in `localStorage`
- Applied on page load
- Toggle updates both UI and stored value

### Visitor Name:
- Saved using `localStorage`
- Loaded automatically when user returns
- Updates greeting message dynamically

---

## 5. Form Validation

### Validation Rules:
- Name: required and minimum length 2
- Email: required and valid format (regex)
- Message: required and minimum length 10

### Process:
1. Prevent form submission
2. Validate each field
3. Show inline error messages
4. Show final success or failure message

---

## 6. Performance Considerations

- Minimal DOM updates
- Reusable functions (e.g., showMessage)
- Limited API results (first 6 repos)
- No external heavy libraries

---

## 7. Testing

The website was tested using:
- Chrome DevTools
- Mobile responsive view
- Manual testing of:
  - API loading
  - search/filter/sort
  - form validation
  - localStorage behavior

---

## 8. User Experience

- Clear instructions provided in UI
- Feedback messages for all actions
- Responsive layout
- Smooth transitions for better interaction
