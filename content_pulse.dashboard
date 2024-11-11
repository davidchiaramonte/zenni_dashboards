---
- dashboard: content_pulse
  title: Content Pulse
  layout: newspaper
  preferred_viewer: dashboards-next
  description: ''
  preferred_slug: j6aDGFVRxb9TOCcrn1SfIb
  elements:
  - title: Unused Looks
    name: Unused Looks
    model: system__activity
    explore: content_usage
    type: looker_grid
    fields: [content_usage.content_id, content_usage.content_title, content_usage.content_type,
      content_usage.api_total, content_usage.embed_total, content_usage.favorites_total,
      content_usage.other_total, content_usage.schedule_total]
    filters:
      content_usage.dashboard_deleted: 'No'
      content_usage.look_deleted: 'No'
      content_usage.content_type: look
    sorts: [content_usage.api_total desc 0]
    limit: 5000
    column_limit: 50
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
    header_font_size: 12
    rows_font_size: 12
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    defaults_version: 1
    listen:
      Days Since Last Accessed (Unused Content): content_usage.days_since_last_accessed
    row: 2
    col: 0
    width: 12
    height: 6
  - title: Unused Dashboards
    name: Unused Dashboards
    model: system__activity
    explore: content_usage
    type: looker_grid
    fields: [content_usage.content_id, content_usage.content_title, content_usage.content_type,
      content_usage.api_total, content_usage.embed_total, content_usage.favorites_total,
      content_usage.other_total, content_usage.schedule_total]
    filters:
      content_usage.dashboard_deleted: 'No'
      content_usage.look_deleted: 'No'
      content_usage.content_type: dashboard
    sorts: [content_usage.api_total desc 0]
    limit: 5000
    column_limit: 50
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
    header_font_size: 12
    rows_font_size: 12
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    defaults_version: 1
    listen:
      Days Since Last Accessed (Unused Content): content_usage.days_since_last_accessed
    row: 2
    col: 12
    width: 12
    height: 6
  - name: ''
    type: text
    title_text: ''
    subtitle_text: ''
    body_text: '[{"type":"h1","children":[{"text":"Unused Content"}],"align":"center"},{"type":"p","children":[{"text":"Remove
      unused Looks and dashboards "},{"type":"a","url":"https://zennianalytics.cloud.looker.com/browse/unused","children":[{"text":"here"}],"id":"c66dy"},{"text":"!"}],"id":"uu8i2","align":"center"}]'
    rich_content_json: '{"format":"slate"}'
    row: 0
    col: 0
    width: 24
    height: 2
  - title: Unused Explores (>=30 days)
    name: Unused Explores (>=30 days)
    model: system__activity
    explore: history
    type: looker_grid
    fields: [query.view, query.model, query.first_query_at, history.query_run_count,
      history.most_recent_query_date]
    filters:
      query.view: "-NULL"
      history.most_recent_query_date: before 30 days ago
      query.model: -"system__activity",-"i__looker"
    sorts: [history.most_recent_query_date]
    limit: 100
    column_limit: 50
    dynamic_fields:
    - table_calculation: first_query_date
      label: First Query Date
      expression: substring(${query.first_query_at},0,10)
      value_format:
      value_format_name:
      _kind_hint: measure
      _type_hint: string
    - table_calculation: days_since_last_query
      label: Days Since Last Query
      expression: diff_days(${history.most_recent_query_date}, now())
      value_format:
      value_format_name:
      _kind_hint: measure
      _type_hint: number
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
    column_order: ["$$$_row_numbers_$$$", query.view, query.model, days_since_last_query,
      history.query_run_count, history.most_recent_query_date, first_query_date]
    show_totals: true
    show_row_totals: true
    series_labels:
      history.most_recent_query_date: Last Query
      first_query_date: First Query
      history.query_run_count: Query Run Count
    series_column_widths:
      query.view: 200
      query.model: 150
      days_since_last_query: 150
    series_cell_visualizations:
      history.query_run_count:
        is_active: true
      days_since_last_query:
        is_active: true
        palette:
          palette_id: 86f8cdb6-9647-deba-106c-ba013817617c
          collection_id: b43731d5-dc87-4a8e-b807-635bef3948e7
          custom_colors:
          - "#4FBC89"
          - "#FCF758"
          - "#F36254"
    truncate_column_names: false
    custom_color_enabled: false
    custom_color: forestgreen
    show_single_value_title: true
    single_value_title: Total Queried
    show_comparison: true
    comparison_type: change
    comparison_reverse_colors: false
    show_comparison_label: true
    hidden_fields: [query.first_query_at]
    note_state: collapsed
    note_display: hover
    note_text: Explores used in the last 90 days that have not been queried in the
      last 30 days.
    defaults_version: 1
    listen: {}
    row: 8
    col: 12
    width: 12
    height: 6
  - title: Unused PDTs
    name: Unused PDTs
    model: system__activity
    explore: content_usage
    type: looker_grid
    fields: [content_usage.content_id, content_usage.content_title, content_usage.content_type,
      content_usage.api_total, content_usage.embed_total, content_usage.favorites_total,
      content_usage.other_total, content_usage.schedule_total]
    filters:
      content_usage.dashboard_deleted: 'No'
      content_usage.look_deleted: 'No'
      content_usage.content_type: pdt
    sorts: [content_usage.api_total desc 0]
    limit: 5000
    column_limit: 50
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
    header_font_size: 12
    rows_font_size: 12
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    x_axis_gridlines: false
    y_axis_gridlines: true
    show_y_axis_labels: true
    show_y_axis_ticks: true
    y_axis_tick_density: default
    y_axis_tick_density_custom: 5
    show_x_axis_label: true
    show_x_axis_ticks: true
    y_axis_scale_mode: linear
    x_axis_reversed: false
    y_axis_reversed: false
    plot_size_by_field: false
    trellis: ''
    stacking: ''
    legend_position: center
    point_style: none
    show_value_labels: false
    label_density: 25
    x_axis_scale: auto
    y_axis_combined: true
    ordering: none
    show_null_labels: false
    show_totals_labels: false
    show_silhouette: false
    totals_color: "#808080"
    defaults_version: 1
    listen:
      Days Since Last Accessed (Unused Content): content_usage.days_since_last_accessed
    row: 8
    col: 0
    width: 12
    height: 6
  - name: " (Copy)"
    type: text
    title_text: " (Copy)"
    subtitle_text: ''
    body_text: '[{"type":"h1","children":[{"text":"Broken Content"}],"align":"center"}]'
    rich_content_json: '{"format":"slate"}'
    row: 14
    col: 0
    width: 24
    height: 2
  - title: Broken Dashboards
    name: Broken Dashboards
    model: system__activity
    explore: history
    type: table
    fields: [dashboard.title, dashboard.link, history.real_dash_id, history.message,
      history.issuer_source, history.count, history.dashboard_user]
    filters:
      history.status: error
      history.source: dashboard
      history.message: "-Access Denied"
      history.workspace_id: "-dev"
      history.created_date: 90 days
    sorts: [history.count desc]
    limit: 100
    column_limit: 50
    color_application:
      collection_id: b43731d5-dc87-4a8e-b807-635bef3948e7
      palette_id: fb7bb53e-b77b-4ab6-8274-9d420d3d73f3
    pinned_columns: {}
    column_order: [dashboard.title, history.message, history.dashboard_user, dashboard.link,
      history.issuer_source]
    show_totals: true
    show_row_totals: true
    show_view_names: false
    show_row_numbers: false
    transpose: false
    truncate_text: true
    size_to_fit: true
    series_labels:
      history.dashboard_user: Impacted Users
      dashboard_creator.name: Creator
    series_column_widths:
      history.real_dash_id: 59
      dashboard.link: 150
      history.message: 550
      history.dashboard_user: 300
      dashboard.title: 275
      history.issuer_source: 215
    series_cell_visualizations:
      history.dashboard_user:
        is_active: true
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: '12'
    rows_font_size: '12'
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    truncate_column_names: true
    hide_totals: false
    hide_row_totals: false
    hidden_fields: [history.count, history.real_dash_id]
    listen: {}
    row: 16
    col: 0
    width: 24
    height: 5
  - title: Broken Schedules
    name: Broken Schedules
    model: system__activity
    explore: scheduled_plan
    type: table
    fields: [scheduled_job.finalized_date, scheduled_job.name, scheduled_job.status_detail,
      scheduled_plan.content_link, scheduled_plan.space_link, scheduled_job.user_id,
      user.name]
    filters:
      scheduled_job.status: failure
    sorts: [scheduled_job.finalized_date desc]
    limit: 100
    column_limit: 50
    column_order: [scheduled_job.name, scheduled_job.status_detail, user.name, scheduled_job.finalized_date,
      scheduled_plan.content_link, scheduled_plan.space_link]
    show_totals: true
    show_row_totals: true
    show_view_names: false
    show_row_numbers: false
    transpose: false
    truncate_text: true
    size_to_fit: true
    series_labels:
      user.name: Creator
      scheduled_job.finalized_date: Job Date
    series_column_widths:
      scheduled_job.finalized_date: 100
      user.name: 200
      scheduled_job.status_detail: 550
      scheduled_plan.content_link: 150
      scheduled_job.name: 275
      scheduled_plan.space_link: 213
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: '12'
    rows_font_size: '12'
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    truncate_column_names: false
    hide_totals: false
    hide_row_totals: false
    hidden_fields: [scheduled_job.user_id]
    listen: {}
    row: 31
    col: 0
    width: 24
    height: 5
  - title: Broken Looks
    name: Broken Looks
    model: system__activity
    explore: history
    type: table
    fields: [look.title, look.link, history.id, history.status, history.message, history.issuer_source,
      history.source, history.count, user.name]
    filters:
      history.status: error
      history.source: look
      history.workspace_id: "-dev"
    sorts: [history.count desc]
    limit: 100
    column_limit: 50
    column_order: [look.title, history.message, user.name, history.id, look.link,
      history.issuer_source]
    show_totals: true
    show_row_totals: true
    show_view_names: false
    show_row_numbers: false
    transpose: false
    truncate_text: true
    size_to_fit: true
    series_column_widths:
      look.title: 275
      history.message: 550
      user.name: 200
      history.id: 100
      look.link: 150
      history.issuer_source: 209
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: '12'
    rows_font_size: '12'
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    truncate_column_names: true
    hide_totals: false
    hide_row_totals: false
    hidden_fields: [history.status, history.source, history.count]
    listen: {}
    row: 21
    col: 0
    width: 24
    height: 5
  - title: Broken PDTs
    name: Broken PDTs
    model: system__activity
    explore: pdt_event_log
    type: table
    fields: [pdt_event_log.view_name, pdt_event_log.model_name, pdt_event_log.action,
      pdt_event_log.action_data, pdt_event_log.connection, pdt_event_log.pdt_create_failures,
      pdt_event_log.pdt_trigger_failures]
    filters:
      pdt_event_log.pdt_create_failures: ">0"
    sorts: [pdt_event_log.pdt_create_failures desc]
    limit: 100
    column_limit: 50
    column_order: [pdt_event_log.view_name, pdt_event_log.model_name, pdt_event_log.action,
      pdt_event_log.action_data, pdt_event_log.pdt_create_failures, pdt_event_log.connection,
      pdt_event_log.pdt_trigger_failures]
    show_totals: true
    show_row_totals: true
    show_view_names: false
    show_row_numbers: false
    transpose: false
    truncate_text: true
    size_to_fit: true
    series_labels:
      pdt_event_log.extract_view_from_table: View Name
    series_column_widths:
      pdt_event_log.model_name: 200
      pdt_event_log.view_name: 275
      pdt_event_log.pdt_create_failures: 300
      pdt_event_log.pdt_trigger_failures: 210
      pdt_event_log.action: 200
      pdt_event_log.action_data: 150
      pdt_event_log.connection: 150
    series_cell_visualizations:
      pdt_event_log.pdt_create_failures:
        is_active: true
      pdt_event_log.pdt_trigger_failures:
        is_active: false
    series_text_format:
      pdt_event_log.pdt_trigger_failures:
        align: left
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: true
    header_text_alignment: left
    header_font_size: '12'
    rows_font_size: '12'
    conditional_formatting: [{type: along a scale..., value: !!null '', background_color: "#3EB0D5",
        font_color: !!null '', color_application: {collection_id: b43731d5-dc87-4a8e-b807-635bef3948e7,
          palette_id: 1e4d66b9-f066-4c33-b0b7-cc10b4810688, options: {steps: 5, constraints: {
              min: {type: minimum}, mid: {type: number, value: 0}, max: {type: maximum}},
            mirror: true, reverse: true, stepped: false}}, bold: false, italic: false,
        strikethrough: false, fields: !!null ''}]
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    truncate_column_names: false
    hide_totals: false
    hide_row_totals: false
    listen: {}
    row: 26
    col: 0
    width: 24
    height: 5
  - name: " (Copy 2)"
    type: text
    title_text: " (Copy 2)"
    subtitle_text: ''
    body_text: '[{"type":"h1","children":[{"text":"New & Trending Content"}],"align":"center"}]'
    rich_content_json: '{"format":"slate"}'
    row: 36
    col: 0
    width: 24
    height: 2
  - title: Popular Content
    name: Popular Content
    model: system__activity
    explore: content_usage
    type: looker_grid
    fields: [content_usage.content_id, content_usage.content_title, content_usage.content_type,
      content_usage.other_total, content_usage.favorites_total, content_usage.schedule_total,
      content_usage.embed_total, content_usage.api_total]
    filters:
      content_usage.days_since_last_accessed: "<30"
      content_usage.dashboard_deleted: 'No'
      content_usage.look_deleted: 'No'
    sorts: [content_usage.other_total desc]
    limit: 50
    column_limit: 50
    column_order: ["$$$_row_numbers_$$$", content_usage.content_title, content_usage.content_type,
      content_usage.other_total, content_usage.embed_total, content_usage.api_total,
      content_usage.favorites_total, content_usage.schedule_total]
    show_totals: true
    show_row_totals: true
    show_view_names: false
    show_row_numbers: true
    transpose: false
    truncate_text: true
    size_to_fit: true
    series_cell_visualizations:
      content_usage.embed_total:
        is_active: false
      content_usage.other_total:
        is_active: false
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: true
    header_text_alignment: left
    header_font_size: '12'
    rows_font_size: '12'
    conditional_formatting: [{type: low to high, value: !!null '', background_color: !!null '',
        font_color: !!null '', palette: {name: White to Green, colors: ["#FFFFFF",
            "#4FBC89"]}, bold: false, italic: false, strikethrough: false, fields: [
          content_usage.other_total]}, {type: low to high, value: !!null '', background_color: !!null '',
        font_color: !!null '', palette: {name: White to Green, colors: ["#FFFFFF",
            "#4FBC89"]}, bold: false, italic: false, strikethrough: false, fields: [
          content_usage.schedule_total]}, {type: low to high, value: !!null '', background_color: !!null '',
        font_color: !!null '', palette: {name: White to Green, colors: ["#FFFFFF",
            "#4FBC89"]}, bold: false, italic: false, strikethrough: false, fields: [
          content_usage.favorites_total]}, {type: low to high, value: !!null '', background_color: !!null '',
        font_color: !!null '', palette: {name: White to Green, colors: ["#FFFFFF",
            "#4FBC89"]}, bold: false, italic: false, strikethrough: false, fields: [
          content_usage.api_total]}, {type: low to high, value: !!null '', background_color: !!null '',
        font_color: !!null '', palette: {name: White to Green, colors: ["#FFFFFF",
            "#4FBC89"]}, bold: false, italic: false, strikethrough: false, fields: [
          content_usage.embed_total]}]
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    truncate_column_names: false
    hide_totals: false
    hide_row_totals: false
    hidden_fields: [content_usage.content_id]
    note_state: collapsed
    note_display: hover
    note_text: All time counts for content that have been accessed within the last
      30 days.
    listen: {}
    row: 38
    col: 0
    width: 12
    height: 6
  - title: Popular Explores
    name: Popular Explores
    model: system__activity
    explore: history
    type: looker_grid
    fields: [query.view, history.query_run_count, user.count, query.model]
    filters:
      history.created_date: 30 days
      history.source: explore
    sorts: [history.query_run_count desc]
    limit: 15
    column_limit: 50
    show_totals: true
    show_row_totals: true
    show_view_names: false
    show_row_numbers: true
    transpose: false
    truncate_text: true
    size_to_fit: true
    series_labels:
      user.count: User Count
    series_cell_visualizations:
      history.query_run_count:
        is_active: true
      user.count:
        is_active: true
    table_theme: white
    limit_displayed_rows: false
    enable_conditional_formatting: false
    header_text_alignment: left
    header_font_size: '12'
    rows_font_size: '12'
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    truncate_column_names: false
    hide_totals: false
    hide_row_totals: false
    listen: {}
    row: 38
    col: 12
    width: 12
    height: 6
  - title: Recently Created Dashboards
    name: Recently Created Dashboards
    model: system__activity
    explore: content_usage
    type: looker_grid
    fields: [content_usage.content_title, dashboard.created_week, content_usage.other_total]
    filters:
      content_usage.content_type: dashboard
      dashboard.created_date: 7 days
      content_usage.dashboard_deleted: 'No'
      content_usage.look_deleted: 'No'
    sorts: [dashboard.created_week desc]
    column_limit: 50
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
    header_font_size: 12
    rows_font_size: 12
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    defaults_version: 1
    listen:
      Days Since Last Accessed (Unused Content): content_usage.days_since_last_accessed
    row: 44
    col: 0
    width: 12
    height: 6
  - title: Recently Created Looks
    name: Recently Created Looks
    model: system__activity
    explore: content_usage
    type: looker_grid
    fields: [content_usage.content_title, look.created_week, content_usage.other_total]
    filters:
      content_usage.content_type: dashboard
      look.created_date: 7 days
      content_usage.dashboard_deleted: 'No'
      content_usage.look_deleted: 'No'
    sorts: [look.created_week desc]
    limit: 5000
    column_limit: 50
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
    header_font_size: 12
    rows_font_size: 12
    conditional_formatting_include_totals: false
    conditional_formatting_include_nulls: false
    x_axis_gridlines: false
    y_axis_gridlines: true
    show_y_axis_labels: true
    show_y_axis_ticks: true
    y_axis_tick_density: default
    y_axis_tick_density_custom: 5
    show_x_axis_label: true
    show_x_axis_ticks: true
    y_axis_scale_mode: linear
    x_axis_reversed: false
    y_axis_reversed: false
    plot_size_by_field: false
    trellis: ''
    stacking: ''
    legend_position: center
    point_style: none
    show_value_labels: false
    label_density: 25
    x_axis_scale: auto
    y_axis_combined: true
    ordering: none
    show_null_labels: false
    show_totals_labels: false
    show_silhouette: false
    totals_color: "#808080"
    defaults_version: 1
    listen:
      Days Since Last Accessed (Unused Content): content_usage.days_since_last_accessed
    row: 44
    col: 12
    width: 12
    height: 6
  filters:
  - name: Days Since Last Accessed (Unused Content)
    title: Days Since Last Accessed (Unused Content)
    type: field_filter
    default_value: ">=60"
    allow_multiple_values: true
    required: false
    ui_config:
      type: advanced
      display: popover
      options:
        min: 0
        max: 120
    model: system__activity
    explore: content_usage
    listens_to_filters: []
    field: content_usage.days_since_last_accessed
