---
title: Propriété canonique PidTagAttachNumber
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachNumber
api_type:
- HeaderDef
ms.assetid: 507e0f2c-383c-4e2f-917b-159913f7234d
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 474ffaf2317cadd214074419f09bb913b1eee4ff
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401502"
---
# <a name="pidtagattachnumber-canonical-property"></a>Propriété canonique PidTagAttachNumber

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient un numéro qui identifie de manière unique la pièce jointe dans un message de son parent. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_ATTACH_NUM  <br/> |
|Identificateur :  <br/> |0x0E21  <br/> |
|Type de données :  <br/> |PT_LONG  <br/> |
|Domaine :  <br/> |Pièce jointe de message  <br/> |
   
## <a name="remarks"></a>Remarques

Banques de messages génèrent et mettre à jour de cette propriété. Le nombre de pièces jointes est la clé de tri secondaire, après la position de rendu dans le tableau des pièces jointes. 
  
 **PR_ATTACH_NUM** est utilisée pour ouvrir la pièce jointe avec la méthode [IMessage::OpenAttach](imessage-openattach.md) . Dans la session d’une application client, la propriété **PR_ATTACH_NUM** d’une pièce jointe du message reste constante dans la mesure où la table de la pièce jointe est ouverte. 
  
La banque de messages propage les modifications à la table à l’aide des méthodes **IMessage::CreateAttach** et **IMessage::DeleteAttach** . À son la banque de messages peut générer des notifications de table sur les tables d’ouvrir une pièce jointe afin que les clients peuvent resynchroniser à ces modifications. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Gère les objets de message et la pièce jointe.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que d’autres noms.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

