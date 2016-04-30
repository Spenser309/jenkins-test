def configs = [
	'centos5_x86_64_centos6_x86_64': [
		'build':  "centos5 && x86_64",
		'host':   "centos6 && x86_64",
		'target': "centos6 && x86_64",
	],
	'centos5_x86_64_centos7_x86_64': [
		'build':  "centos5 && x86_64",
		'host':   "centos7 && x86_64",
		'target': "centos7 && x86_64"
	],
	'native_centos6_x86_64': [
		'build':  "centos6 && x86_64",
		'host':   "centos6 && x86_64",
		'target': "centos6 && x86_64",
	],
	'native_centos7_x86_64': [
		'build':  "centos7 && x86_64",
		'host':   "centos7 && x86_64",
		'target': "centos7 && x86_64",
	]
];

configs.each { name, config ->
	stage("Build ${name}");
	node(config.build) {
		echo('Build');
	};
/*
	stage("Build Unit Tests $name")
	node(config.host) {
		echo('Build Unit Tests')
	}

	stage("Run Unit Tests $name")
	node(config.target) {
		echo('Run Unit Tests')
	}

	stage("Install $name")
	node(config.build) {
		echo('Install')
	}

	stage("Build Integration Tests $name")
	node(config.host) {
		echo("Build Integration Tests")
	}

	stage("Run Integration Tests $name")
	node(config.target) {
		echo("Run Integration Tests")
	}

	stage("Build Performance Tests $name")
	node(config.host) {
		echo("Build Performance Tests")
	}

	stage("Run Performance Tests $name")
	node(config.target) {
		echo("Run Performance Tests")
	}

	stage("Deploy $name")
	node(config.build) {
		echo("Deploying")
	}
*/
}
