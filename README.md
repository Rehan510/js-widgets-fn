const obj = {
    user: {
        profile: {
            name: 'John Doe',
            contact: {
                email: 'john@example.com',
            }
        }
    }
};

// Retrieve the email safely
const email = window.getObjValue(obj, 'user.profile.contact.email', 'no-email@example.com');
console.log(email); // Output: 'john@example.com'

// Attempt to retrieve a non-existent property
const phone = window.getObjValue(obj, 'user.profile.contact.phone', 'no-phone');
console.log(phone); // Output: 'no-phone'

// Attempt to use a non-object
const invalid = window.getObjValue(null, 'user.profile.contact.email', 'no-data');
console.log(invalid); // Output: 'no-data'
