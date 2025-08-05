# Schemas

JSON schemas for AI-optimized business content structure validation.

## Contents
- `business-profile.json` - Core business information schema
- `service-catalog.json` - Service offerings structure schema  
- `client-profile.json` - Client business profile template schema
- `performance-metrics.json` - Success metrics and KPI schema

## Usage
These schemas validate the structure of your AI-optimized content to ensure maximum compatibility with AI language models.

```javascript
// Example schema validation
const Ajv = require('ajv');
const ajv = new Ajv();

const businessSchema = require('./business-profile.json');
const validate = ajv.compile(businessSchema);

const isValid = validate(yourBusinessData);
if (!isValid) {
    console.log(validate.errors);
}
