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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339374"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a>Propriété canonique PidTagPrimarySendAccount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne qui nomme le premier serveur utilisé pour envoyer le message.
  
|||
|:-----|:-----|
|Propriétés associées :  <br/> |PR_PRIMARY_SEND_ACCOUNT  <br/> |
|Identificateur :  <br/> |0x0E28  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Compte  <br/> |
   
## <a name="remarks"></a>Remarques

Spécifie le premier serveur qu’un client doit utiliser pour envoyer le message. Le format de ces propriétés dépend de l’implémentation. Ces propriétés peuvent être utilisées par le client pour déterminer le serveur vers lequel diriger le courrier, mais elles sont facultatives et la valeur n’a aucune signification pour le serveur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server de protocole associées.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
### <a name="header-files"></a>Fichiers d’en-tête

Mapidefs.h
  
> Fournit des définitions de type de données.
    
Mapitags.h
  
> Contient les définitions des propriétés répertoriées en tant que propriétés associées.
    
## <a name="see-also"></a>Voir aussi



[Propriétés MAPI](mapi-properties.md)
  
[Propriétés canoniques MAPI](mapi-canonical-properties.md)
  
[Mappage des noms de propriétés canoniques aux noms MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mappage des noms MAPI aux noms de propriétés canoniques](mapping-mapi-names-to-canonical-property-names.md)

