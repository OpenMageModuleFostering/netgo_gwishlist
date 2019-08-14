*****************
Usage in CMS page
*****************


1) Open app/design/frontend/YourThemePackage/YourThemeName/template/catalog/product/list.phtml file:

2) Find the wishlist code:
  
   <?php if ($this->helper('wishlist')->isAllow()) : ?>

	<li>
		<a href="<?php echo $this->helper('wishlist')->getAddUrl($_product) ?>"

			<?php echo $this->__('Add to Wishlist') ?>

		</a>
	</li>
	
    <?php endif; ?>

3) Replace the above code with this one:

   <?php echo Mage::helper('netgo_gwishlist')->getUrl($_product);   ?>


