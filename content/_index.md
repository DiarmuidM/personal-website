---
# Leave the homepage title empty to use the site title
title: Diarmuid McDonnell
date: 2023-09-14
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: About me
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Lecturer in Social Sciences
          company: University of the West of Scotland
          company_url: 'https://www.uws.ac.uk/'
          company_logo: 
          location: Glasgow
          date_start: '2021-08-23'
          date_end: ''
        - title: Research Fellow in Social Policy
          company: Third Sector Research Centre, University of Birmingham
          company_url: 'https://www.birmingham.ac.uk/research/tsrc/index.aspx'
          company_logo: 
          location: Birmingham
          date_start: '2017-11-01'
          date_end: '2021-08-01'
  - block: grants
    content:
      title: Research and teaching grants
      text: '*The ecosystem of support organisations during the Cost-of-Living crisis*, British Academy Early Career Researcher Network Seed Funding, Principal Investigator. Award value: £1,380.'
      text: '*Improving access to and use of organisation-level data on the third sector and civil society*, Economic and Social Research Council, Co-Investigator. Award value: £680,919.'
      text: '*Creative and Computational Methods for Working with Digital Footprint Data*, Scottish Graduate School of Social Science and the Scottish Graduate School for Arts & Humanities, Principal Investigator. Award value: £1,000.'
      text: '*Data for Good: The Voluntary, Community and Social Enterprise Sector in Britain*, Festival of Social Science, Co-Investigator. Award values: £1,500.'
      text: '*Mission Accomplished? A Cross-national Examination of Charity Dissolution*, British Academy, Principal Investigator. Award value: £9,879.65.'
  - block: teaching
    content:
      title: Teaching
      text: 'I have methodological and teaching interests in the use of administrative data, quantitative methods and computational social science. I have been commissioned to deliver and develop training courses and materials for the National Centre for Research Methods, Scottish Graduate School of Social Science, and Wales Institute of Social and Economic Research and Data.'
      text: 'Many of my teaching materials are public and can be found at my Github account: [https://github.com/DiarmuidM](https://github.com/DiarmuidM)'
  - block: collection
    id: posts
    content:
      title: Recent Posts
      subtitle: ''
      text: ''
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        exclude_featured: false
        exclude_future: false
        exclude_past: false
        publication_type: ""
      # Choose how many pages you would like to offset by
      offset: 0
      # Page order: descending (desc) or ascending (asc) date.
      order: desc
    design:
      # Choose a layout view
      view: compact
      columns: '2'
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
  - block: collection
    id: featured
    content:
      title: Featured Publications
      filters:
        folders:
          - publication
        featured_only: true
    design:
      columns: '2'
      view: card
  - block: collection
    content:
      title: Recent Publications
      text: |-
        {{% callout note %}}
        Quickly discover relevant content by [filtering publications](./publication/).
        {{% /callout %}}
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
---
