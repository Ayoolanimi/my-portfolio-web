---
title: Home
slug: /
sections:
  - type: GenericSection
    subtitle: ''
    text: >+
      > **Most decisions are not binary, and there are usually better answers
      waiting to be found if you do the analysis and involve the right
      people...**


      ```
                                  Jamie Dimon
      ```

    actions: []
    media:
      url: /images/face-swap.png
      altText: Welcome to my portfolio. Here is a quote I go by
      elementId: ''
      type: ImageBlock
    elementId: ''
    colors: bg-dark-fg-light
    styles:
      self:
        alignItems: center
        flexDirection: row
        padding:
          - pt-16
          - pl-16
          - pb-16
          - pr-16
    backgroundImage:
      type: BackgroundImage
      altText: altText of the image
      backgroundSize: cover
      backgroundPosition: center
      backgroundRepeat: no-repeat
      opacity: 50
      url: /images/mikey-harris-kw0z6RyvC0s-unsplash.jpg
  - type: FeaturedItemsSection
    title:
      text: Skills and Interests
      color: text-dark
      styles:
        self:
          textAlign: center
      type: TitleBlock
    subtitle: ''
    items:
      - type: FeaturedItem
        title: Hard Skills
        subtitle: ''
        text: |+
          *   Data Analysis and Visualization

          *   Web Scraping and Data Extraction

          *   Database Design and Management

          *   Data Manipulation and Preprocessing

          *   Exploratory Data Analysis

          *   Predictive Models

          *   Artificial Intelligence (AI)

          *   Deep Learning

          *   Machine Learning (ML)

          *   Natural Language Processing (NLP)

        actions: []
        elementId: null
        colors: bg-neutralAlt-fg-dark
        styles:
          self:
            padding:
              - pt-8
              - pl-8
              - pb-8
              - pr-8
            borderRadius: x-large
            flexDirection: row
            justifyContent: center
            textAlign: left
        image:
          type: ImageBlock
          altText: Lightning bolt symbol on red background
          elementId: ''
          url: /images/icon1.svg
          styles:
            self:
              borderRadius: x-large
      - title: Soft Skills
        subtitle: ''
        text: |+
          *   Leadership

          *   Attention to detail

          *   Critical thinking

          *   Problem Solving

          *   Cross-functional team collaboration

          *   Communication

          *   Multi-tasking

        image:
          url: /images/icon2.svg
          altText: Featured icon two
          elementId: ''
          type: ImageBlock
        actions: []
        colors: bg-neutralAlt-fg-dark
        styles:
          self:
            padding:
              - pt-8
              - pl-8
              - pb-8
              - pr-8
            borderRadius: x-large
            flexDirection: row
            textAlign: left
            justifyContent: center
        type: FeaturedItem
      - title: Interests
        subtitle: ''
        text: |+
          *   Reading

          *   Music

          *   Sports

          *   Traveling

          *   Web-Surfing

          *   Continuous Learning and Development

        image:
          url: /images/icon3.svg
          altText: Featured icon three
          elementId: ''
          type: ImageBlock
        actions: []
        colors: bg-neutralAlt-fg-dark
        styles:
          self:
            padding:
              - pt-8
              - pl-8
              - pb-8
              - pr-8
            borderRadius: x-large
            flexDirection: row
        type: FeaturedItem
    actions: []
    elementId: ''
    variant: three-col-grid
    colors: bg-neutral-fg-dark
    styles:
      self:
        padding:
          - pb-16
          - pt-16
          - pl-16
          - pr-16
        justifyContent: center
      subtitle:
        textAlign: center
  - subtitle: Tools and Proficiencies
    images:
      - type: ImageBlock
        altText: Image alt text placeholder
        elementId: ''
        styles:
          self:
            borderRadius: medium
        url: /images/power bi - Copy.png
      - type: ImageBlock
        url: /images/f1bd4d1d1c7765d826285decce3129dd.png
        altText: Image alt text placeholder
        elementId: ''
        styles:
          self:
            borderRadius: medium
      - type: ImageBlock
        altText: Image alt text placeholder
        elementId: ''
        styles:
          self:
            borderRadius: medium
      - type: ImageBlock
        url: /images/9ccc53a59405b484a68a48002625743c.png
        altText: Image alt text placeholder
        elementId: ''
        styles:
          self:
            borderRadius: medium
      - type: ImageBlock
        url: /images/mysql Copy.png
        altText: Image alt text placeholder
        elementId: ''
        styles:
          self:
            borderRadius: medium
      - type: ImageBlock
        altText: Image alt text placeholder
        elementId: ''
        styles:
          self:
            borderRadius: medium
      - type: ImageBlock
        url: /images/tableau - Copy.png
        altText: Image alt text placeholder
        elementId: ''
        styles:
          self:
            borderRadius: medium
    motion: move-to-left
    colors: bg-light-fg-dark
    styles:
      self:
        justifyContent: center
      subtitle:
        textAlign: center
    type: ImageGallerySection
  - posts:
      - content/pages/blog/case-study-1.md
      - content/pages/blog/case-study-2.md
      - content/pages/blog/case-study-3.md
    showThumbnail: true
    showDate: true
    showAuthor: true
    variant: three-col-grid
    colors: bg-light-fg-dark
    styles:
      self:
        padding:
          - pt-16
          - pl-16
          - pb-16
          - pr-16
        justifyContent: center
    type: FeaturedPostsSection
    hoverEffect: move-up
    showExcerpt: false
  - title: Divider
    colors: bg-light-fg-dark
    styles:
      self:
        padding:
          - pt-7
          - pl-7
          - pb-7
          - pr-7
    type: DividerSection
  - title:
      text: Awards
      color: text-dark
      styles:
        self:
          textAlign: center
      type: TitleBlock
    subtitle: ''
    text: |-
      Aenean eros ipsum, interdum quis dignissim non, sollicitudin vitae nisl.
      Aenean vel aliquet elit, at blandit ipsum. Sed eleifend felis sit amet
      erat molestie, hendrerit malesuada justo ultrices. Nunc volutpat at erat
      vitae interdum. Ut nec massa eget lorem blandit condimentum et at risus.
    media:
      title: Title of the video
      url: /images/placeholder-video.mp4
      controls: false
      aspectRatio: '16:9'
      styles:
        self:
          padding:
            - pt-2
            - pb-2
            - pl-2
            - pr-2
          borderColor: border-dark
          borderStyle: solid
          borderWidth: 1
          borderRadius: large
      type: VideoBlock
      autoplay: true
      loop: true
      muted: true
    badge:
      label: ''
      color: text-primary
      styles:
        self:
          textAlign: center
      type: Badge
    colors: bg-light-fg-dark
    styles:
      self:
        flexDirection: col
        justifyContent: center
      subtitle:
        textAlign: center
    type: GenericSection
  - title: Divider
    colors: bg-light-fg-dark
    styles:
      self:
        padding:
          - pt-7
          - pl-7
          - pb-7
          - pr-7
    type: DividerSection
  - title:
      text: Awards
      color: text-primary
      styles:
        self:
          textAlign: center
      type: TitleBlock
    subtitle: This section showcases my badges and certifications.
    items:
      - title: Cisco Data Analyst
        tagline: ''
        subtitle: 'For verification, click:'
        text: |
          https\://www\.credly.com/badges/dc1a2f6a-c64f-487d-a736-6ed8d6649d72
        image:
          url: /images/cisco badge.png
          altText: Placeholder Image
          styles:
            self:
              borderRadius: x-large
          type: ImageBlock
        colors: bg-light-fg-dark
        styles:
          self:
            padding:
              - pt-8
              - pl-8
              - pb-8
              - pr-8
            borderRadius: x-large
            flexDirection: col
        type: FeaturedItem
      - title: IBM Python for Data Science
        tagline: ''
        subtitle: 'For verification, click:'
        text: |
          https\://www\.credly.com/badges/f3258452-76f3-4742-a404-1d217f548450
        image:
          url: /images/python for data science.png
          altText: Placeholder image
          styles:
            self:
              borderRadius: x-large
          type: ImageBlock
        colors: bg-light-fg-dark
        styles:
          self:
            padding:
              - pt-8
              - pl-8
              - pb-8
              - pr-8
            borderRadius: x-large
            flexDirection: col
        type: FeaturedItem
      - title: IBM Data Analysis using Python
        tagline: ''
        subtitle: 'For verification, click:'
        text: |
          https\://www\.credly.com/badges/72ab73aa-c4ca-49e0-9e5e-84f846f0b361
        image:
          url: /images/data analysis with python.png
          altText: Placeholder image
          styles:
            self:
              borderRadius: x-large
          type: ImageBlock
        colors: bg-light-fg-dark
        styles:
          self:
            padding:
              - pt-8
              - pl-8
              - pb-8
              - pr-8
            borderRadius: x-large
            flexDirection: col
        type: FeaturedItem
    variant: three-col-grid
    colors: bg-neutral-fg-dark
    styles:
      self:
        padding:
          - pt-16
          - pl-8
          - pb-16
          - pr-8
        justifyContent: center
      subtitle:
        textAlign: center
    type: FeaturedItemsSection
  - title:
      text: Please fill this form
      color: text-dark
      type: TitleBlock
    subtitle: ''
    text: |-
      Aenean eros ipsum, interdum quis dignissim non, sollicitudin vitae nisl.
      Aenean vel aliquet elit, at blandit ipsum. Sed eleifend felis sit amet
      erat molestie, hendrerit malesuada justo ultrices. Nunc volutpat at erat
      vitae interdum. Ut nec massa eget lorem blandit condimentum et at risus.
    media:
      fields:
        - name: name
          label: Name
          hideLabel: true
          placeholder: Your name
          isRequired: true
          width: full
          type: TextFormControl
        - name: email
          label: Email
          hideLabel: true
          placeholder: Your email
          isRequired: true
          width: full
          type: EmailFormControl
        - name: message
          label: Message
          hideLabel: true
          placeholder: Your message
          width: full
          type: TextareaFormControl
      elementId: contact-form
      styles:
        self:
          padding:
            - pt-6
            - pb-6
            - pl-6
            - pr-6
          borderColor: border-dark
          borderStyle: solid
          borderWidth: 1
          borderRadius: large
      type: FormBlock
      submitButton:
        type: SubmitButtonFormControl
        label: Submit
        showIcon: false
        icon: arrowRight
        iconPosition: right
        style: primary
        elementId: null
    badge:
      label: Contact me
      color: text-primary
      type: Badge
    colors: bg-light-fg-dark
    type: GenericSection
seo:
  type: Seo
  metaTitle: Home - Demo Site
type: PageLayout
isDraft: false
---
