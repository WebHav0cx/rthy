import React, { useState } from "react";

function NumberInput() {
  const [inputValue, setInputValue] = useState("");
  const [errorMessage, setErrorMessage] = useState("");

  const handleInputChange = (e) => {
    let value = e.target.value.replace(/\D/g, ""); // Ensure only numbers

    if (value.length > 10) {
      setErrorMessage("Max number is 10 digits");
    } else {
      setErrorMessage(""); // Clear error message if valid
    }

    setInputValue(value);
  };

  return (
    <div className="w-full">
      <input
        type="text"
        placeholder="Enter Phone Number"
        className="border p-2 rounded w-full mb-2"
        value={inputValue}
        onChange={handleInputChange}
        onKeyDown={(e) => {
          if (e.key === "ArrowUp" || e.key === "ArrowDown") {
            e.preventDefault(); // Disables arrow increment/decrement
          }
        }}
        style={{ appearance: "textfield" }} // Hides number arrows
      />
      {errorMessage && <p className="text-red-600 text-sm">{errorMessage}</p>}
    </div>
  );
}

export default NumberInput;
