---
title: Enregistrement des propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ed0c14f9-3dcf-49ad-928e-ba872d4d6b5a
ms.openlocfilehash: 72186596972247c8d5bf7857c134e7f3de2c2830
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63374074"
---
# <a name="saving-mapi-properties"></a>Enregistrement des propriétés MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
De nombreux objets sont pris en charge par un modèle de traitement de transaction dans lequel les modifications apportées aux propriétés ne sont pas définitives tant qu’elles n’ont pas été apportées ultérieurement. Alors que les modifications apportées aux propriétés sont gérées par les méthodes [IMAPIProp::SetProps](imapiprop-setprops.md) et [IMAPIProp::D eleteProps](imapiprop-deleteprops.md) , l’étape de validation est gérée par [IMAPIProp::SaveChanges](imapiprop-savechanges.md). Ce n’est qu’après un appel réussi à **SaveChanges** que la version la plus récente des propriétés d’un objet est accessible. 
  
Lorsque **SaveChanges renvoie** la valeur d’MAPI_E_OBJECT_CHANGED, il s’agit d’un avertissement signalant qu’un autre client validation simultanément les modifications apportées à l’objet. Selon le fournisseur qui implémente l’objet, plusieurs clients peuvent ouvrir un objet en appelant sa méthode **OpenEntry** avec l’indicateur MAPI_MODIFY, ce qui leur donne un accès en lecture/écriture. L’objet renvoyé par un appel **OpenEntry** de ce type est un instantané des données de stockage. Chaque tentative ultérieure de modification de ces données peut modifier la tentative précédente. 
  
Lors de la MAPI_E_OBJECT_CHANGED de **SaveChanges**, un client a la possibilité de : 
  
- Faites une copie de l’objet pour contenir les modifications.
    
- Effectuer un autre appel **à SaveChanges**, en spécifiant FORCE_SAVE. 
    
**L’appel de SaveChanges** avec l FORCE_SAVE’indicateur de modification modifie l’enregistrer précédent et rend permanentes les modifications d’un client. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

