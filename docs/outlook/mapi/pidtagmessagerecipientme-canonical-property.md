---
title: Propriété canonique PidTagMessageRecipientMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325619"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a>Propriété canonique PidTagMessageRecipientMe

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient la valeur TRUE si cet utilisateur de messagerie est spécifiquement nommé en tant que destinataire principal (to), copie carbone (CC) ou copie carbone invisible (CCI) de ce message et ne fait pas partie d'une liste de distribution. 
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_MESSAGE_RECIP_ME  <br/> |
|Identificateur :  <br/> |0x0059  <br/> |
|Type de données :  <br/> |PT_BOOLEAN  <br/> |
|Domaine :  <br/> |Messagerie générale  <br/> |
   
## <a name="remarks"></a>Remarques

Cette propriété offre un moyen pratique de déterminer si le nom d'utilisateur apparaît explicitement dans la liste des destinataires, sans examiner toutes les entrées de la liste. La valeur représente l'opération logique **or** des propriétés **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) et **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)), et les informations CCI (qui n'apparaissent pas dans une propriété). 
  
Cette propriété facilite le traitement automatisé des messages reçus au moment de l'accusé de réception. À l'option du fournisseur de transport, cette propriété contient soit la valeur FALSe, soit elle n'est pas incluse si l'utilisateur de messagerie n'est pas répertorié directement dans la table des destinataires. 
  
La remise des messages résultant de l'expansion de la liste de distribution n'entraîne pas la définition de cette propriété. Le destinataire doit être nommé explicitement. 
  
Les messages non envoyés ne définissent généralement pas cette propriété, **PR_MESSAGE_CC_ME**ou **PR_MESSAGE_TO_ME**. S'ils sont présents dans les messages auxquels l'utilisateur peut accéder dans les banques de messages publics, dans les magasins privés des autres utilisateurs, dans les fichiers sur le disque ou dans d'autres messages reçus, ils contiennent généralement les valeurs auxquelles ils ont été définis lors de la dernière utilisation d'un fournisseur de transport. le message a été remis. 
  
## <a name="related-resources"></a>Ressources associées

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références à des spécifications de protocole Exchange Server connexes.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets message électronique.
    
### <a name="header-files"></a>Fichiers d'en-tête

Mapidefs. h
  
> Fournit des définitions de type de données.
    
Mapitags. h
  
> Contient les définitions des propriétés figurant en tant que noms de substitution.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

