---
title: Propriété canonique PidTagAttachRendering
description: Décrit la propriété canonique PidTagAttachRendering, qui contient un métafichier Microsoft Windows avec des informations de rendu pour une pièce jointe.
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
ms.openlocfilehash: d00feae5e3139ce1733ac0edb88404ea395c1f71
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817164"
---
# <a name="pidtagattachrendering-canonical-property"></a>Propriété canonique PidTagAttachRendering

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un métafichier Microsoft Windows avec des informations de rendu pour une pièce jointe. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_RENDERING  <br/> |
|Identificateur :  <br/> |0x3709  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

L’objectif de cette propriété est de fournir une icône ou une autre représentation picturale qui peut être affichée dans le message parent au point de pièce jointe. Cette représentation inclut généralement le nom de la pièce jointe, le cas échéant, et la nature de la pièce jointe, telle qu’un document Microsoft Office Word. Une application cliente peut utiliser cette représentation dans l’affichage du message. 
  
Pour un fichier attaché, cette propriété représente généralement une icône pour le fichier. 
  
Pour un message joint, cette propriété n’est généralement pas définie. Une application cliente qui doit afficher un message joint doit obtenir sa propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), appeler [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour un pointeur vers l’objet d’informations de formulaire correspondant, ouvrir l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) sur cet objet et utiliser **GetProps** pour récupérer la **propriété PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
  
Pour un objet OLE statique incorporé, cette propriété contient un métafichier Microsoft Windows qui peut être utilisé pour dessiner la représentation de pièce jointe dans une fenêtre. 
  
Pour un objet OLE dynamique incorporé, le client doit utiliser les données OLE pour générer les informations de rendu. 
  
Dans tous les cas, l’application cliente doit savoir que cette propriété a généralement une taille de plusieurs centaines d’octets et qu’elle est soumise à une troncation dans la table de pièces jointes. Si un client souhaite afficher la pièce jointe à partir de cette propriété sans ouvrir la pièce jointe elle-même, elle doit fonctionner dans la règle de troncation de table. Pour plus d’informations, consultez [Utilisation de colonnes volumineuses](working-with-large-columns.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient des définitions de propriétés répertoriées en tant que noms secondaires.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI à des noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

