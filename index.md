<html>
    <script type='text/javascript'>
	  function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
      			
      window.addEventListener("onEmbeddedMessagingReady", () => {            
			console.log( "Inside Prechat API!!" );
			embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields( {'QueueName' : 'EdloeFinch' } );
			});
			window.addEventListener("onEmbeddedMessagingReady", e => {
			    embeddedservice_bootstrap.prechatAPI.setVisiblePrechatFields({
			        "_firstName": {
			            "value": "",
			            "isEditableByEndUser": true
			        },
			        "_lastName": {
			            "value": "",
			            "isEditableByEndUser": true
			        },
			        "_email": {
			            "value": "",
			            "isEditableByEndUser": true
			        },
			        "_subject": {
			            "value": "",
			            "isEditableByEndUser": true
				}
			    });
			});
			embeddedservice_bootstrap.init(
				'00DO400000C6iHG',
				'Edloe_Finch_Messaging_Chat',
				'https://exemplis--partial.sandbox.my.site.com/ESWEdloeFinchMessaging1749156695294',
				{
					scrt2URL: 'https://exemplis--partial.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	  };
     </script>
    <script type='text/javascript' src='https://exemplis--partial.sandbox.my.site.com/ESWEdloeFinchMessaging1749156695294/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</html>
