Console

// Formatting
console.log(‘Bam bam %s and I do it %d times", ‘bam", 24);

// Grouping - may be nested
console.groupCollapsed('Group');
console.log('bam!');
console.groupEnd();

// Counting in loops
console.count('fam');

// Time measuring
console.time('String id')
console.timeEnd('String id');

// Table pretty print
console.table(object, [identifiers]);

// OMG CSS
console.log('%c OMG! OMG! OMG! OMG! ', 'background: #123; color: #bada55');

