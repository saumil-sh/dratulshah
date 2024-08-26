---
title: Home
layout: parent
parent: none
order: 1
parts:
  - hair
  - skin
  - head
  - body
apart: head
types:
  - memberships
  - medical
  - fellowships
  - cosmetology
  - management
  - law
atype: memberships
days:
  - appointment
  - monday
  - tuesday
  - wednesday
  - thursday
aday: monday
---
<div class="fh5co-hero">
	<div class="fh5co-overlay"></div>
	<div class="fh5co-cover" data-stellar-background-ratio="0.52" style="background-image: url(assets/img/home-image.jpg);">
		<div class="desc animate-box">
			<div class="container">
				<div class="row">
					<div class="col-md-8 col-md-offset-5">
						<h2>Love of beauty is <b>Taste</b>.<br>
						The creation of beauty is <b>Art</b>.</h2>
						<p><span>&ensp;- Ralph Waldo Emerson</span></p>
					</div>
				</div>
				<div class="row">
					<div class="col-md-7 col-md-offset-4">
						<p><h3><b>Taking care of your Appearance</b><br>
						Anti Ageing has to start before the effect of age, gravity, hormones, and nutritional imbalances take over.</h3></p>
						<p><h3><b>Dr. Atulkumar Shah</b><br>
						University qualified expert in the field of cosmetology, cosmetic surgery, anti ageing, and plastic surgery.</h3></p>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>
<!-- end:fh5co-hero -->

<div id="fh5co-schedule-section" class="fh5co-lightgray-section">
	<div id="specialties" class="container">
		<div class="row">
			<div class="col-md-10 col-md-offset-1">
				<div class="heading-section text-center animate-box">
					<h2>Specialties</h2>
					<!-- <p>Dr Atulkumar Shah is consultant in cosmetic, plastic, reconstructive, and burns surgery practicing in Vadodara (Baroda - BRC - BDQ). Active member and past President of Vadodara branch of Indian Medical Association, he was also Honorary Secretery of Association of Plastic Surgeons of India for 6 years from 2010.</p> -->
				</div>
			</div>
		</div>
		<div class="row animate-box">
			<div class="col-md-10 col-md-offset-1 text-center">
				<ul class="specialty">
					{% for part in page.parts %}
  					<li><a href="#" {% if part == page.apart %}class="active"{% endif %} data-spec="{{ part }}">{{ part | capitalize }}</a></li>
					{% endfor %}
				</ul>
			</div>
			<div class="row text-center">
				<div class="col-md-12 specialty-container">
					{% for bodypart in page.parts %}
					<div class="specialty-content {% if bodypart == page.apart %}active{% endif %}" data-day="{{ bodypart }}">
						{% assign specialties = site.specialties | where: "part", bodypart %}
						{%- for spec in specialties -%}
						<div class="col-md-3 col-sm-6">
							<div class="program program-schedule">
								<h3>{{- spec.name -}}</h3>
								<span>{{- spec.procedure -}}</span>
							</div>
						</div>
						{%- endfor -%}
					</div>
					<!-- END spec-content -->
					{%- endfor -%}
				</div>
			</div>
		</div>
	</div>
</div>
<!-- end: fh5co-parallax -->

<div class="separator">
	<div class="overlay"></div>
	<div class="container">
		<div class="row">
			<div class="col-md-8 col-md-offset-2 col-sm-12 col-sm-offset-0 col-xs-12 col-xs-offset-0 text-center fh5co-table">
				<div class="fh5co-intro fh5co-table-cell animate-box fadeInUp animated">
					<h1 class="text-center">Credentials</h1>
					<p>Dr Atulkumar Shah is consultant in cosmetic, plastic, reconstructive, and burns surgery practicing in Vadodara (Baroda - BRC - BDQ). Active member and past President of Vadodara branch of Indian Medical Association, he was also Honorary Secretery of Association of Plastic Surgeons of India for 6 years from 2010.</p>
				</div>
			</div>
		</div>
	</div>
</div>
<!-- end: fh5co-parallax -->

<div id="fh5co-schedule-section" class="fh5co-lightgray-section">
	<div class="container">
		<!-- <div class="row">
			<div class="col-md-10 col-md-offset-1">
				<div class="heading-section text-center animate-box">
					<h2>Credentials</h2>
					<p>Dr Atulkumar Shah is consultant in cosmetic, plastic, reconstructive, and burns surgery practicing in Vadodara (Baroda - BRC - BDQ). Active member and past President of Vadodara branch of Indian Medical Association, he was also Honorary Secretery of Association of Plastic Surgeons of India for 6 years from 2010.</p>
				</div>
			</div>
		</div> -->
		<div class="row animate-box">
			<div class="col-md-10 col-md-offset-1 text-center">
				<ul class="credential">
					{% for cred_type in page.types %}
  					<li><a href="#" {% if cred_type == page.atype %}class="active"{% endif %} data-cred="{{ cred_type }}">{{ cred_type | capitalize }}</a></li>
					{% endfor %}
				</ul>
			</div>
			<div class="row text-center">
				<div class="col-md-12 credential-container">
					{% for cred_type in page.types %}
					<div class="credential-content {% if cred_type == page.atype %}active{% endif %}" data-day="{{ cred_type }}">
						{% assign creds = site.credentials | where: "type", cred_type %}
						{%- for cred in creds -%}
						<div class="col-md-3 col-sm-6">
							<div class="program program-schedule">
								{%- if cred.image == nil -%}
								<i class="fa-solid fa-{{ cred.graphic }}"></i>
								{%- else -%}
								<img src="assets/img/{{ cred.image }}" alt="">
								{%- endif -%}
								<small>{{- cred.year -}}</small>
								<h3>{{- cred.name -}}</h3>
								<small>{{- cred.specialization -}}</small>
								<span>{{- cred.organization -}}</span>
							</div>
						</div>
						{%- endfor -%}
					</div>
					<!-- END cred-content -->
					{%- endfor -%}
				</div>
			</div>
		</div>
	</div>
</div>
<!-- end: fh5co-parallax -->

<div class="separator">
	<div class="overlay"></div>
	<div class="container">
		<div class="row">
			<div class="col-md-8 col-md-offset-2 col-sm-12 col-sm-offset-0 col-xs-12 col-xs-offset-0 text-center fh5co-table">
				<div class="fh5co-intro fh5co-table-cell animate-box fadeInUp animated">
					<h1 class="text-center">Consult</h1>
					<p>Dr. Atul Shah is available for consultation.</p>
				</div>
			</div>
		</div>
	</div>
</div>
<!-- end: fh5co-parallax -->

<div id="fh5co-schedule-section" class="fh5co-lightgray-section">
	<div id="appointment" class="container">
		<!-- <div class="row">
			<div class="col-md-10 col-md-offset-1">
				<div class="heading-section text-center animate-box">
					<h2>Credentials</h2>
					<p>Dr Atulkumar Shah is consultant in cosmetic, plastic, reconstructive, and burns surgery practicing in Vadodara (Baroda - BRC - BDQ). Active member and past President of Vadodara branch of Indian Medical Association, he was also Honorary Secretery of Association of Plastic Surgeons of India for 6 years from 2010.</p>
				</div>
			</div>
		</div> -->
		<div class="row animate-box">
			<div class="col-md-10 col-md-offset-1 text-center">
				<ul class="schedule">
					{% for day in page.days %}
  					<li><a href="#" {% if day == page.aday %}class="active"{% endif %} data-sched="{{ day }}">{{ day | capitalize }}</a></li>
					{% endfor %}
				</ul>
			</div>
			<div class="row text-center">
				<div class="col-md-12 schedule-container">
					{% assign midday = "AM, PM" | split: ", "%}
					{% for weekday in page.days %}
					<div class="schedule-content {% if weekday == page.aday %}active{% endif %}" data-day="{{ weekday }}">
						{% assign slots = site.slots | where: "day", weekday %}
						{{ slot.organization }}
						{%- for slot in slots -%}
						<div class="col-md-3 col-sm-6">
							<div class="program program-schedule">
								{%- if slot.image == nil -%}
								<i class="fa-solid fa-{{ slot.graphic }}"></i>
								{%- else -%}
								<img src="assets/img/{{ slot.image }}" alt="">
								{%- endif -%}
								{% assign start_id = slot.start | divided_by: 12 %}
								{% assign stop_id = slot.stop | divided_by: 12 %}
								{% if slot.start != nil %}
								<small>{{ slot.start -}} {{ midday[start_id] }} - {{ slot.stop -}} {{ midday[stop_id] }}</small>
								{% endif %}
								<h3>{{- slot.organization -}}</h3>
								<span>{{- slot.where -}}</span>
							</div>
						</div>
						{%- endfor -%}
					</div>
					<!-- END sched-content -->
					{%- endfor -%}
				</div>
			</div>
		</div>
	</div>
</div>
<!-- end: fh5co-parallax -->