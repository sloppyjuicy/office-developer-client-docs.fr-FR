---
title: Propriété canonique PidTagAttachRendering
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachRendering
api_type:
- HeaderDef
ms.assetid: 1f31f7f4-fbda-4337-95e5-5474dd1bf84a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a1df3ba8e57f1e91894b88d7e8a72feb681e13dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785739"
---
# <a name="pidtagattachrendering-canonical-property"></a>Propriété canonique PidTagAttachRendering

  
  
**S’applique à**: Outlook 
  
Contient un métafichier Microsoft Windows avec des informations de rendu d’une pièce jointe. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_RENDERING  <br/> |
|Identificateur :  <br/> |0x3709  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Zone :  <br/> |Pièce jointe du message  <br/> |
   
## <a name="remarks"></a>Remarques

L’objectif de cette propriété est de fournir une icône ou une autre représentation graphique qui peut être affichée dans le message parent au moment de la pièce jointe. Représentation inclut généralement le nom de la pièce jointe, le cas échéant et la nature de la pièce jointe, par exemple un document Microsoft Office Word. Une application cliente peut utiliser cette représentation dans l’affichage du message. 
  
Pour une pièce jointe, cette propriété illustre généralement une icône pour le fichier. 
  
Pour un message attaché, cette propriété n’est généralement pas définie. Une application cliente ayant besoin d’afficher un message joint doit obtenir sa propriété **PR_MESSAGE_CLASS** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md)), appelez [IMAPIFormMgr::ResolveMessageClass](imapiformmgr-resolvemessageclass.md) pour un pointeur vers l’objet d’informations de formulaire correspondant, Ouvrez l’interface [IMAPIFormInfo](imapiforminfoimapiprop.md) sur cet objet, puis **GetProps** permet de récupérer les **PR_ICON** ([PidTagIcon](pidtagicon-canonical-property.md)) ou la propriété **PR_MINI_ICON** ([PidTagMiniIcon](pidtagminiicon-canonical-property.md)). 
  
Pour un objet OLE incorporé statique, cette propriété contient un métafichier Microsoft Windows qui peut être utilisé pour dessiner la représentation sous forme de pièce jointe dans une fenêtre. 
  
Pour un objet OLE incorporé dynamique, le client doit utiliser les données OLE pour générer les informations de rendu. 
  
Dans tous les cas, l’application cliente Sachez que cette propriété est généralement plusieurs centaines d’octets de taille et est soumis à la troncation de la table des pièces jointes. Si un client souhaite afficher la pièce jointe à partir de cette propriété sans ouvrir la pièce jointe lui-même, il doit fonctionner dans la règle de troncature de table. Pour plus d’informations, voir [utilisation des colonnes de grande taille](working-with-large-columns.md). 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage de noms de propriété canonique aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage de noms MAPI pour les noms de propriété canonique](mapping-mapi-names-to-canonical-property-names.md)

