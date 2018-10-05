---
title: Propriété canonique PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPrimarySendAccount
api_type:
- COM
ms.assetid: 2f268b3b-2e4c-4aea-8879-bdd0ac1df35c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2c32cc61fea63cd38215c30e04e8a467d4901cc9
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387313"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a>Propriété canonique PidTagPrimarySendAccount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne qui nomme le premier serveur est utilisé pour envoyer le message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|Identificateur :  <br/> |0x0E28  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Compte  <br/> |
   
## <a name="remarks"></a>Remarques

Spécifie le premier serveur qu’un client doit utiliser pour envoyer le message. Le format de ces propriétés est dépend de l’implémentation. Peut être utilisé par le client pour déterminer le serveur pour diriger le courrier par le biais de ces propriétés, mais est facultatives et la valeur est dépourvu de signification sur le serveur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications du protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications du protocole Exchange Server associées.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et les opérations qui sont autorisées pour les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
MAPITAGS.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

