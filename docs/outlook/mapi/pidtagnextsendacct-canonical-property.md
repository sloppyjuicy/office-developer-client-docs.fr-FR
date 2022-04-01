---
title: Propriété canonique PidTagNextSendAcct
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PidTagNextSendAcct
api_type:
- HeaderDef
ms.assetid: b7429c2e-0d9d-4921-9f56-9ecad817f8cb
description: Spécifie le serveur qu’un client tente actuellement d’utiliser pour envoyer des messages électroniques. Le format de cette propriété dépend de l’implémentation.
ms.openlocfilehash: f5e77a650810224c1bc097ad3c43ed9111c968a3
ms.sourcegitcommit: 1f8a789204b2498101d24fb5136e8ed6ad026c13
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/29/2022
ms.locfileid: "64523731"
---
# <a name="pidtagnextsendacct-canonical-property"></a>Propriété canonique PidTagNextSendAcct

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie le serveur qu’un client tente actuellement d’utiliser pour envoyer des messages électroniques.
  
|Propriété |Valeur |
|:-----|:-----|
|Propriétés associées :  <br/> |PR_NEXT_SEND_ACCT  <br/> |
|Identificateur :  <br/> |0x0E29  <br/> |
|Type de données :  <br/> |PT_UNICODE  <br/> |
|Domaine :  <br/> |Outlook application  <br/> |
   
## <a name="remarks"></a>Remarques

Le format de cette propriété dépend de l’implémentation. Cette propriété peut être utilisée par le client pour déterminer le serveur vers lequel diriger le courrier électronique, mais elle est facultative et la valeur n’a aucune signification pour le serveur.
  
## <a name="related-resources"></a>Ressources connexes

### <a name="protocol-specifications"></a>Spécifications de protocole

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fournit des références aux spécifications Exchange Server protocole associés.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Convertit les objets RFC2445, RFC2446 et RFC2447 de l’IETF, ainsi que les objets de rendez-vous et de réunion.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Spécifie les propriétés et opérations autorisées pour les objets de message électronique.
    
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

