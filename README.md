bullify
=======

Turn this:

	list = [
	    'First Main Point.',
	    [
	        'First main - first subpoint',
	        'First main - second subpoint',
	        'First main - third subpoint'
	    ],
	    'Second Main Point.',
	    [
	        'Second main - first subpoint',
	        'Second main - second subpoint',
	        [
	            'Second main - second subpoint - first point',
	            'Second main - second subpoint - second point',
	            'Second main - second subpoint - third point'
	        ],
	        'Second main - third subpoint'
	    ]
	]
	
Into this:
	
	<ol>
        <li>
            First Main Point.
            <ol>
                <li>First main - first subpoint</li>
                <li>First main - second subpoint</li>
                <li>First main - third subpoint</li>
            </ol>
        </li>
        <li>
            Second Main Point.
            <ol>
                <li>Second main - first subpoint</li>
                <li>Second main - second subpoint
                    <ol>
                        <li>Second main - second subpoint - first point</li>
                        <li>Second main - second subpoint - second point</li>
                        <li>Second main - second subpoint - third point</li>
                    </ol>
                </li>
                <li>Second main - third subpoint</li>
            </ol>
        </li>
    </ol>
    
By doing this:

	var orderedList = new Bullify('ol', 'li');
	document.getElementById('bullify').innerHTML = orderedList.bullify(list)
