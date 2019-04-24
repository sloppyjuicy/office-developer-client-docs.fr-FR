---
title: Enregistrement des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 5d4653492028151d7e19a5d5490c8c8949002a4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283085"
---
# <a name="saving-mapi-properties"></a>Enregistrement des propriétés MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
De nombreux objets prennent en charge un modèle de transaction de traitement dans lequel les modifications apportées aux propriétés ne sont pas permanentes tant qu'elles n'ont pas été validées ultérieurement. Tandis que les modifications apportées aux propriétés sont gérées par les méthodes [IMAPIProp:: SetProps](imapiprop-setprops.md) et [IMAPIProp::D eleteprops](imapiprop-deleteprops.md) , l'étape de validation est gérée par [IMAPIProp:: SaveChanges](imapiprop-savechanges.md). Il n'est pas possible d'accéder à la version la plus récente des propriétés d'un objet après un appel réussi à **SaveChanges** . 
  
Lorsque **SaveChanges** renvoie la valeur d'erreur MAPI_E_OBJECT_CHANGED, il s'agit d'un avertissement indiquant qu'un autre client valide simultanément les modifications apportées à l'objet. Selon le fournisseur qui implémente l'objet, il est possible que plusieurs clients ouvrent correctement un objet en appelant sa méthode **OpenEntry** avec l'indicateur MAPI_MODIFY défini, en leur donnant accès en lecture/écriture. L'objet renvoyé par un appel **OpenEntry** est une capture instantanée des données de stockage. Chaque tentative ultérieure de modification de ces données peut remplacer la tentative précédente. 
  
Lors de la réception de MAPI_E_OBJECT_CHANGED à partir d' **SaveChanges**, un client a la possibilité de: 
  
- Effectuez une copie de l'objet pour conserver les modifications.
    
- Appeler **SaveChanges**en spécifiant FORCE_SAVE. 
    
L'appel de **SaveChanges** avec l'indicateur FORCE_SAVE remplace l'enregistrement précédent et rend les modifications d'un client permanentes. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

