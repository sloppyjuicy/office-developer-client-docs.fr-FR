---
title: Intégration à Office à partir d'applications iOS
manager: soliver
ms.date: 06/04/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: f3a277ba-7ba1-4eea-83b5-915b409f3093
description: Office pour iOS fournit une solution extensible qui permet l'intégration à des applications tierces. Cet article explique comment effectuer une intégration à Office à partir de votre application iOS en transférant les utilisateurs de votre application vers Office, puis en les renvoyant vers votre application.
ms.openlocfilehash: 90de84b8b99fb276157bb3b36290fa6e0d8838d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596728"
---
# <a name="integrate-with-office-from-ios-applications"></a>Intégration à Office à partir d'applications iOS

Office pour iOS fournit une solution extensible qui permet l'intégration à des applications tierces. Cet article explique comment effectuer une intégration à Office à partir de votre application iOS en transférant les utilisateurs de votre application vers Office, puis en les renvoyant vers votre application.
  
Vous pouvez permettre aux utilisateurs exécutant Office sur un périphérique iOS d'ouvrir et de modifier des fichiers stockés dans SharePoint ou OneDrive à partir de n'importe quelle application, puis les renvoyer rapidement vers l'application d'origine lorsqu'ils ont terminé la modification du fichier. Pour ce faire, vous transférez les fichiers à Office via des gestionnaires de protocole et vous vous assurez qu'Office est appelé d'une manière qu'Office peut comprendre.
  
Lorsqu'un utilisateur a terminé la modification d'un fichier, il peut sélectionner la flèche de retour dans l'application Office pour fermer le document et revenir à l'application de stockage d'origine, pour autant que vous transmettiez des informations spécifiques à l'application Office à son lancement.
  
## <a name="verify-that-office-has-been-installed"></a>Vérifier qu'Office a été installé

Votre application référente doit d'abord vérifier qu'une application Office particulière est installée. Les applications Office suivantes peuvent être installées sur des périphériques iOS pour l'affichage et la modification de documents :
  
- Excel
    
- OneNote
    
- PowerPoint
    
- Word
    
Utilisez la méthode [canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html) pour déterminer si votre application peut ouvrir la ressource. Cette méthode prend l'URL de la ressource comme paramètre, puis renvoie **No** si l'application qui accepte l'URL n'est pas disponible. Si **canOpenURL** renvoie **No**, vous devez inviter l'utilisateur à installer Office.
  
### <a name="prompt-the-user-to-install-office"></a>Inviter l'utilisateur à installer Office

 Si une application Office particulière n'est pas installée, vous pouvez utiliser un objet [SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html) pour afficher l'App Store iTunes dans votre application et montrer à l'utilisateur l'application Office à installer. Le tableau suivant indique l'identifiant iTunes à utiliser pour appeler chaque application Office dans Store Kit Product View Controller. 
  
|**Application Office**|**Identifiant iTunes**|
|:-----|:-----|
|Excel  <br/> |[https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-excel/id586683407?mt=8&amp;uo=4) <br/> |
|OneNote (iPhone)  <br/> |[https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-onenote-for-iphone/id410395246?mt=8&amp;uo=4) <br/> |
|PowerPoint  <br/> |[https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-powerpoint/id586449534?mt=8&amp;uo=4) <br/> |
|Word  <br/> |[https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4](https://itunes.apple.com/us/app/microsoft-word/id586447913?mt=8&amp;uo=4) <br/> |
   
## <a name="invoke-office"></a>Appeler Office

Lorsque l'application Office est installée, votre application référente peut appeler Office en transmettant les détails suivants : 
  
- Protocole Office
    
- Mode d'ouverture
    
- URL
    
- Protocole de transmission retour
    
- Contexte de document
    
Format de schéma :
  
 `<Office protocol><open mode>|u|<URL>|p|<passback protocol>|c|<document context>`
  
L'exemple suivant montre une demande d'appel de fichier Word pour modification :
  
 `ms-word:ofe|u|https://contoso/Q4/budget.docx|p|clouddrive|c|folderviewQ4`
  
### <a name="office-protocols"></a>Protocoles Office

Le tableau suivant répertorie les protocoles pour chaque application Office. 
  
|**Application**|**Protocole**|
|:-----|:-----|
|Excel  <br/> |ms-excel:  <br/> |
|OneNote  <br/> |onenote:  <br/> |
|PowerPoint  <br/> |ms-powerpoint:  <br/> |
|Word  <br/> |ms-word:  <br/> |
   
### <a name="open-mode"></a>Mode d'ouverture

Les applications Office peuvent ouvrir les fichiers directement en mode d'affichage (ofv) ou de modification (ofe), ce dernier étant le mode par défaut. 
  
Format de schéma :
  
 `<ofv or ofe>`
  
### <a name="url"></a>URL

L'URL comprend trois parties : 
  
- Déclaration indiquant que le fichier est ouvert pour modification (ofe)
    
- Descripteur de l'URL (|u|)
    
- URL
    
L'URL doit être codée et il doit s'agir d'un lien direct vers le fichier (et non d'une redirection). Si le format de l'URL ne peut pas être géré par Office ou en cas d'échec du téléchargement, Office ne renvoie pas l'utilisateur vers l'application appelante. 
  
Format de schéma :
  
 `|u|<document URL>`
  
### <a name="passback-protocol-optional"></a>Protocole de transmission retour (facultatif)

Si vous voulez qu'Office renvoie les utilisateurs vers votre application iOS lorsqu'ils choisissent la flèche de retour, l'application appelante doit utiliser le protocole de transmission retour, qui comprend le descripteur « |p| » suivi du protocole de l'application (sans signe deux-points). Assurez-vous que votre application peut gérer correctement la réponse d'Office.
  
Format de schéma :
  
 `|p|<passback protocol>`
  
### <a name="document-context-optional"></a>Contexte de document (facultatif)

Office n'utilise pas le contexte du document, mais l'application référente peut en avoir besoin lorsque Office transmet un utilisateur en retour. Si vous voulez que le contexte de document soit renvoyé vers votre application, utilisez le descripteur « |c| » suivi du contexte que vous voulez comme chaîne. Office ne limite pas la longueur de la chaîne, au-delà des limites imposées par le système d'exploitation.
  
Format de schéma :
  
 `|c|<document context>`
  
## <a name="return-users-to-the-referring-application"></a>Renvoyer les utilisateurs vers l'application référente

Pour des raisons de sécurité, Office renvoie uniquement les utilisateurs vers l'application référente si le fichier a été ouvert. Lorsque l'utilisateur sélectionne la flèche de retour, Office répond à l'application appelante avec le protocole de transmission retour, le mode d'ouverture, l'URL, l'état de téléchargement en attente et le contexte de document. L'état de téléchargement en attente utilise le descripteur |z| et prend la valeur Oui ou Non.
  
Format de schéma :
  
 `<app protocol>:ofe|u|<URL>|z|<yes or no>|c|<doc context> Example: clouddrive:ofe|u|https://contoso/Q4/budget.docx|z|no|c|folderviewQ4`
  
## <a name="see-also"></a>Voir aussi
<a name="bk_addresources"> </a>

- [Méthode canOpenURL](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [Classe UIApplication](https://developer.apple.com/library/ios/documentation/UIKit/Reference/UIApplication_Class/index.html)
    
- [Objet SKProductViewController](https://developer.apple.com/library/ios/documentation/StoreKit/Reference/SKITunesProductViewController_Ref/index.html)
    

