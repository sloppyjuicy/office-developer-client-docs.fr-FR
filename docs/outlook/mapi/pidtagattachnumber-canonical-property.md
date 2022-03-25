---
title: Propriété canonique PidTagAttachNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: Contient un nombre qui identifie de manière unique la pièce jointe dans son message parent. Les magasins de messages génèrent et conservent cette propriété.
ms.openlocfilehash: 1d1c2dbe36981b03bd5318b26862f0859d685b12
ms.sourcegitcommit: 138c9e15adc07c6ecd740257872aaee6a1a1a7fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64405222"
---
# <a name="pidtagattachnumber-canonical-property"></a>Propriété canonique PidTagAttachNumber

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un nombre qui identifie de manière unique la pièce jointe dans son message parent. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_NUM  <br/> |
|Identificateur :  <br/> |0x0E21  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Les magasins de messages génèrent et conservent cette propriété. Le numéro de pièce jointe est la clé de tri secondaire, après la position de rendu, dans le tableau des pièces jointes. 
  
 **PR_ATTACH_NUM** permet d’ouvrir la pièce jointe avec la méthode [IMessage::OpenAttach](imessage-openattach.md) . Dans la session d’une application cliente, la propriété **PR_ATTACH_NUM** d’une pièce jointe de message reste constante tant que la table de pièces jointes est ouverte. 
  
La magasin de messages propage les modifications apportées à la table à l’aide des méthodes **IMessage::CreateAttach** et **IMessage::D eleteAttach** . À son option, la boutique de messages peut générer des notifications de tableau sur les tables de pièces jointes ouvertes afin que les clients peuvent resynchroniser ces modifications. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et de pièce jointe.
    
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

