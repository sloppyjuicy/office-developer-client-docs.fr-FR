---
title: Propriété canonique PidTagMessageRecipientMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: Contient TRUE si cet utilisateur de messagerie est spécifiquement nommé comme destinataire principal (À), Cc ou Cci de ce message et ne fait pas partie d’une liste de distribution.
ms.openlocfilehash: ff6d38a98ec369c0d7162eb0d3778ecf25c33a0a
ms.sourcegitcommit: c68b7b7f98b3ff9e6de37ee5877adcad2e5e71d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63741552"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a>Propriété canonique PidTagMessageRecipientMe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient TRUE si cet utilisateur de messagerie est spécifiquement nommé comme destinataire principal (À), Copie carbone (CC) ou Copie carbone non voyante (Cci) de ce message et ne fait pas partie d’une liste de distribution. 
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_RECIP_ME  <br/> |
|Identificateur :  <br/> |0x0059  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété fournit un moyen pratique de déterminer si le nom d’utilisateur apparaît explicitement dans la liste des destinataires, sans examiner toutes les entrées de la liste. La valeur représente l’opération **logique OR** des propriétés **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) et **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), ainsi que les informations Cci (qui n’apparaissent pas dans une propriété). 
  
Cette propriété permet la gestion automatisée des messages reçus au moment de la réception. À l’option du fournisseur de transport, cette propriété contient false ou n’est pas incluse si l’utilisateur de messagerie n’est pas répertorié directement dans la table des destinataires. 
  
La remise des messages qui résulte de l’extension de la liste de distribution ne provoque pas la mise en place de cette propriété. Le destinataire doit être nommé explicitement. 
  
Les messages non envoyés ne définissent généralement pas cette propriété, **PR_MESSAGE_CC_ME** ou **PR_MESSAGE_TO_ME**. S’ils sont présents dans des messages accessibles par l’utilisateur dans des magasins de messages publics, dans des magasins privés d’autres utilisateurs, dans des fichiers sur disque ou incorporés à d’autres messages reçus, ils contiennent généralement les valeurs à laquelle ils ont été fixés la dernière fois qu’un fournisseur de transport a remis le message. 
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées sur les objets de message électronique.
    
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

