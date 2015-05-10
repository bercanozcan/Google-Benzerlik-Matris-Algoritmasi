<?php 

	/*
	*	Twitter: http://twitter.com/bercanozcan
	*	GitHub: http://github.com/bercanozcan
	*/

	function bunumudediniz($word,$memory){
		
		$yuzde=array();
		
		foreach($memory as $h){	
			$benzer = levenshtein($word, $h);
			array_push($yuzde,$benzer);
		}
		
		foreach(array_keys($yuzde, min($yuzde)) as $siralama){
			similar_text($memory[$siralama], $word, $benzerliyuzdesi); 
			return array($memory[$siralama],round($benzerlikyuzdesi));
		} 
	}

	$word = 'elmmmaa';
	$memory = array('kalem','elma','duvar','korna','iğne');
	$cikti = bunumudediniz($word,$memory);

	echo "Bunu mu demek istemiştiniz ".$cikti[0].PHP_EOL;
	echo "Benzerlik yüzdesi %".$cikti[1];

?>
