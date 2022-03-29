---
title: Propriété canonique PidTagConversationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 92c7f46713981977cfe92f331694fd632f3152c8
ms.sourcegitcommit: 331e2bc18fb14cc9868d28ca29cb5eda85c8f154
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/25/2022
ms.locfileid: "64455950"
---
# <a name="pidtagconversationkey-canonical-property"></a>Propriété canonique PidTagConversationKey

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la clé de conversation utilisée dans Microsoft Outlook uniquement lors de la localisation **d’IPM. Messages MessageManager**, tels que le message qui contient l’historique de téléchargement d’un compte POP3 (Post Office Protocol). Cette propriété a été Microsoft Exchange Server. 
  
|Propriété|Valeur|
|:-----|:-----|
|Propriétés associées :  <br/> |PR_CONVERSATION_KEY  <br/> |
|Identificateur :  <br/> |0x000B  <br/> |
|Type de données :  <br/> |PT_BINARY  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Lorsque vous accédez à des messages électroniques en tant que conversations et que vous convertissez des propriétés de message au [format TNEF (Transport-Neutral Encapsulation Format),](transport-neutral-encapsulation-format-tnef.md) n’utilisez pas cette propriété . utilisez plutôt les propriétés canoniques [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) et [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) . 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Microsoft Exchange Server de protocole.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les objets de message électronique.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Code et décode les objets de message et de pièce jointe dans une représentation de flux efficace.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que noms de remplacement.
    
## <a name="see-also"></a>Voir aussi



[Sous-arbre IPM](ipm-subtree.md)
  
[Dossiers spéciaux MAPI](mapi-special-folders.md)
  
[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

