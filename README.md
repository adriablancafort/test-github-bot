// Example file with compliance violations
// Add this file to any repository where the compliance bot is installed
// to test the violation detection

// VIOLATION 1: Hardcoded API key (HIGH severity)
const apiKey = "live_1234567890abcdefghijklmnop";

// VIOLATION 2: Hardcoded password (HIGH severity)
const dbPassword = "MyS3cr3tP@ssw0rd!";

// VIOLATION 3: AWS credentials (HIGH severity)
const config = {
  aws_access_key_id: "AKIAIOSFODNN7EXAMPLE",
  aws_secret_access_key: "wJalrXUtnFEMI/K7MDENG/bPxRfiCYEXAMPLEKEY"
};

// VIOLATION 4: Console statements (LOW severity)
console.log("Debug info:", apiKey);
console.error("Error occurred");

// VIOLATION 5: TODO comment (LOW severity)
// TODO: Fix this later

// VIOLATION 6: Disabled linting (MEDIUM severity)
// eslint-disable-next-line no-unused-vars
const unusedVariable = "test";

// VIOLATION 7: TypeScript ignore (MEDIUM severity)
// @ts-ignore
const problematicCode = somethingUndefined;

// VIOLATION 8: Unsafe eval (HIGH severity)
function executeCode(code) {
  return eval(code);
}

// This file should trigger a compliance report with:
// - 4 high severity violations
// - 2 medium severity violations
// - 2 low severity violations

module.exports = { apiKey, dbPassword, config };