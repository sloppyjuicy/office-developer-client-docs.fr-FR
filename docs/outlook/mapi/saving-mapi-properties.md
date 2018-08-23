---
title: L’enregistrement des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 5125fc8f3e36087a05802c38127a8402ae67d468
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576301"
---
# <a name="saving-mapi-properties"></a>L’enregistrement des propriétés MAPI

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
De nombreux objets prennent en charge un modèle de transaction de traitement selon laquelle les modifications apportées aux propriétés ne sont pas apportées définitive jusqu'à ce qu’ils soient validées à une date ultérieure. Tandis que les modifications apportées aux propriétés sont gérées par les méthodes [IMAPIProp::SetProps](imapiprop-setprops.md) et [IMAPIProp::DeleteProps](imapiprop-deleteprops.md) , l’étape de validation est gérée par [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Il n’est pas qu’après un appel réussi **SaveChanges** que la version la plus récente des propriétés d’un objet est accessible. 
  
Lorsque **l’argument SaveChanges** renvoie la valeur d’erreur MAPI_E_OBJECT_CHANGED, il s’agit d’un avertissement indiquant qu’un autre client est validation simultanément des modifications à l’objet. Il est possible, selon le fournisseur de l’implémentation de l’objet, permettant aux clients plusieurs correctement ouvrir un objet en appelant la méthode **OpenEntry** avec l’indicateur n’est défini, en leur donnant accès en lecture/écriture. L’objet est renvoyé à partir de ces qu'un appel **OpenEntry** est une capture instantanée des données de stockage. Toute tentative ultérieure pour modifier ces données peut remplacer la tentative précédente. 
  
Lors de la réception MAPI_E_OBJECT_CHANGED de **SaveChanges**, un client a la possibilité de : 
  
- Effectuez une copie de l’objet pour contenir les modifications.
    
- Appeler un autre **SaveChanges**, spécifiant FORCE_SAVE. 
    
Appel de **SaveChanges** avec l’indicateur FORCE_SAVE remplace l’enregistrement précédent et modifie d’un client définitive. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

