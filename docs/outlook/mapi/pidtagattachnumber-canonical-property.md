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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: b594a7cd69b6c75b064e30868f3cce0070519246
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550833"
---
# <a name="pidtagattachnumber-canonical-property"></a>Propriété canonique PidTagAttachNumber

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un nombre qui identifie de manière unique la pièce jointe dans son message parent. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_NUM  <br/> |
|Identificateur :  <br/> |0x0E21  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Les magasins de messages génèrent et conservent cette propriété. Le numéro de pièce jointe est la clé de tri secondaire, après la position de rendu, dans le tableau des pièces jointes. 
  
 **PR_ATTACH_NUM** permet d’ouvrir la pièce jointe avec la méthode [IMessage::OpenAttach.](imessage-openattach.md) Au sein de la session d’une application cliente, la propriété **PR_ATTACH_NUM** d’une pièce jointe de message reste constante tant que la table de pièces jointes est ouverte. 
  
La magasin de messages propage les modifications apportées à la table à l’aide des méthodes **IMessage::CreateAttach** et **IMessage::D eleteAttach.** À son option, la boutique de messages peut générer des notifications de tableau sur les tables de pièces jointes ouvertes afin que les clients peuvent resynchroniser ces modifications. 
  
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

