# Custom-Taxonomy



/* Register Custom Post Types********************************************/
<?php
	add_action( 'init', 'create_post_type' );
	function create_post_type() {
		register_post_type( 'testimonial',
			array(
				'labels' => array(
					'name' => __( 'Testimonial' ),
					'singular_name' => __( 'Testimonial' ),
					'add_new' => __( 'Add New' ),
					'add_new_item' => __( 'Add New Testimonial' ),
					'edit_item' => __( 'Edit Testimonial' ),
					'new_item' => __( 'New Testimonial' ),
					'view_item' => __( 'View Testimonial' ),
					'not_found' => __( 'Sorry, we couldn\'t find the Testimonial you are looking for.' )
				),
			'public' => true,
			'publicly_queryable' => false,
			'exclude_from_search' => true,
			'menu_position' => 14,
			'has_archive' => false,
			'hierarchical' => false, 
			'capability_type' => 'page',
			'rewrite' => array( 'slug' => 'testimonial' ),
			'supports' => array( 'title', 'editor', 'custom-fields' )
			)
		);
	}
  ?>
