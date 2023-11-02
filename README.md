function ConvertHandler() {
  this.galToL = 3.78541;

  this.convert = function (input) {
    // Extract the numerical value and unit from input
    const num = parseFloat(input);
    const unit = input.match(/[a-zA-Z]+/g)[0];

    // Perform the conversion based on the unit
    let result;
    switch (unit) {
      case 'gal':
        result = num * this.galToL;
        break;
      case 'L':
        result = num / this.galToL;
        break;
      // Handle other unit conversions similarly
    }

    return result;
  };
}

module.exports = ConvertHandler;
# QA-Testing
