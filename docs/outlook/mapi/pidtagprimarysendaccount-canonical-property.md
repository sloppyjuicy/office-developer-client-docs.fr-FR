---
title: Propriété canonique PidTagPrimarySendAccount
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.PidTagPrimarySendAccount
api_type:
- COM
ms.assetid: 2f268b3b-2e4c-4aea-8879-bdd0ac1df35c
description: Contient une chaîne qui nomme le premier serveur utilisé pour envoyer le message. Le format de ces propriétés dépend de l’implémentation.
ms.openlocfilehash: ff7249b6edca37f71aba814e9ae688d6519d2910
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523562"
---
# <a name="pidtagprimarysendaccount-canonical-property"></a>Propriété canonique PidTagPrimarySendAccount

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Contient une chaîne qui nomme le premier serveur utilisé pour envoyer le message.
  
|Propriété |Valeur |
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
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
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

