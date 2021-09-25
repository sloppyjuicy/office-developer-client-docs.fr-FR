---
title: Propriété canonique PidTagAttachRendering
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0571d7726c17334867138346f92e99deccf9f259
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59600455"
---
# <a name="pidtagattachrendering-canonical-property"></a>Propriété canonique PidTagAttachRendering

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un métafichier Microsoft Windows avec les informations de rendu d’une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_RENDERING  <br/> |
|Identificateur :  <br/> |0x3709  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

L’objectif de cette propriété est de fournir une icône ou une autre représentation de l’icône qui peut être affichée dans le message parent au point de la pièce jointe. Cette représentation inclut généralement le nom de la pièce jointe, le cas besoin, et la nature de la pièce jointe, telle qu’Microsoft Office document Word. Une application cliente peut utiliser cette représentation dans l’affichage du message. 
  
Pour un fichier joint, cette propriété offre généralement une icône pour le fichier. 
  
Pour un message joint, cette propriété n’est généralement pas définie. Une application cliente qui doit restituer un message joint doit obtenir sa propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), appeler [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour un pointeur vers l’objet d’informations de formulaire correspondant, ouvrir l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) sur cet objet et utiliser **GetProps** pour récupérer la propriété **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
  
Pour un objet OLE statique incorporé, cette propriété contient un métafichier Microsoft Windows qui peut être utilisé pour dessiner la représentation de pièce jointe dans une fenêtre. 
  
Pour un objet OLE dynamique incorporé, le client doit utiliser les données OLE pour générer les informations de rendu. 
  
Dans tous les cas, l’application cliente doit savoir que cette propriété a généralement une taille de plusieurs centaines d’octets et est soumise à la troncation dans la table des pièces jointes. Si un client souhaite restituer la pièce jointe à partir de cette propriété sans ouvrir la pièce jointe elle-même, elle doit fonctionner dans la règle de troncation de table. Pour plus d’informations, [voir Working with Large Columns](working-with-large-columns.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets message et pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

