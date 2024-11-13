---
- dashboard: dashboard_update_monitoring
  title: Dashboard Update Monitoring
  layout: newspaper
  preferred_viewer: dashboards-next
  description: ''
  preferred_slug: 3CZfcIjqjt4fPKnwDV9U6v
  elements:
  - title: Recently Updated Dashboards
    name: Recently Updated Dashboards
    model: system__activity
    explore: dashboard
    type: looker_grid
    fields: [dashboard.updated_time, updated_by.name, dashboard.id, dashboard.title,
      dashboard.link]
    filters:
      dashboard.moved_to_trash: 'No'
    sorts: [dashboard.updated_time desc]
    limit: 500
    column_limit: 50
    query_timezone: America/Los_Angeles
    show_view_names: false
    show_row_numbers: true
    transpose: false
    truncate_text: true
    hide_totals: false
    hide_row_totals: false
    size_to_fit: true
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: '12'
    rows_font_size: '12'
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    show_sql_query_menu_options: false
    show_totals: true
    show_row_totals: true
    truncate_header: false
    minimum_column_width: 75
    series_labels:
      updated_by.name: Updater Name
      dashboard.title: Dashboard Title
      dashboard.id: Dashboard ID
      dashboard.link: Link to Dashboard
    defaults_version: 1
    listen:
      Folder Name: folders.name
    row: 0
    col: 0
    width: 24
    height: 12
  - title: Dashboard Events
    name: Dashboard Events
    model: system__activity
    explore: event_attribute
    type: looker_grid
    fields: [event.created_time, event_attribute.value, event.id, event.name, user.id,
      user.name]
    filters:
      event.name: '"update_dashboard","update_dashboard_element","update_dashboard_filter","update_dashboard_layout_component"'
    sorts: [event.created_time desc]
    limit: 500
    column_limit: 50
    query_timezone: America/Los_Angeles
    show_view_names: false
    show_row_numbers: true
    transpose: false
    truncate_text: true
    hide_totals: false
    hide_row_totals: false
    size_to_fit: true
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: '12'
    rows_font_size: '12'
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    show_sql_query_menu_options: false
    show_totals: true
    show_row_totals: true
    truncate_header: false
    minimum_column_width: 75
    series_labels:
      event_attribute.value: Dashboard ID
      event.id: Event ID
      event.name: Type of Event
      user.id: User ID
      user.name: User Name
      event.created_time: Event Timestamp
    defaults_version: 1
    listen: {}
    row: 12
    col: 0
    width: 24
    height: 6
  filters:
  - name: Folder Name
    title: Folder Name
    type: field_filter
    default_value: -Shared,-"Under_Development"
    allow_multiple_values: true
    required: false
    ui_config:
      type: advanced
      display: popover
    model: system__activity
    explore: dashboard
    listens_to_filters: []
    field: folders.name
