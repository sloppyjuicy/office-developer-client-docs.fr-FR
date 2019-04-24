---
title: Agir en tant que fournisseur de carnets d'adresses hôte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 202d4b4391de7553e39e50dc527df5502ebcefb3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331268"
---
# <a name="acting-as-a-host-address-book-provider"></a>Agir en tant que fournisseur de carnets d'adresses hôte

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur hôte est un fournisseur de carnets d'adresses qui inclut des destinataires d'autres fournisseurs dans ses conteneurs et s'appuie sur l'implémentation des destinataires par les autres fournisseurs pour contrôler partiellement leur maintenance. Un fournisseur d'hôte utilise les identificateurs de modèle de ces destinataires étrangers pour lier les données de ces destinataires au code dans le fournisseur étranger. Ce processus de liaison est initié lorsque votre fournisseur récupère la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) d'un destinataire et la transmet dans un appel à [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md). 
  
Lorsque votre fournisseur appelle **IMAPISupport:: OpenTemplateID**, MAPI établit une correspondance avec l' **MAPIUID** dans l'identificateur de modèle avec un **MAPIUID** enregistré par un fournisseur et appelle la méthode [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) du fournisseur. Le fournisseur étranger peut renvoyer un pointeur vers l'objet Property de votre fournisseur, vers sa propre implémentation d'objet Property ou vers une implémentation qui encapsule l'objet de votre fournisseur. Le pointeur renvoyé est placé dans le contenu du paramètre _lppMAPIPropNew_ . 
  
Votre fournisseur peut choisir d'appeler **IMAPISupport:: OpenTemplateID** avec l'indicateur FILL_ENTRY défini. Définissez cet indicateur lorsque le destinataire est en cours de création ou lorsqu'un long moment s'est écoulé depuis que votre fournisseur a actualisé les propriétés du destinataire. Une utilisation courante de l'indicateur FILL_ENTRY est de maintenir la synchronisation d'un destinataire de votre fournisseur avec l'original. L'implémentation de ce type de planification de synchronisation améliore les performances. 
  
 **Pour conserver la synchronisation d'un destinataire étranger**
  
1. Déterminez un intervalle approprié pour les mises à jour périodiques. 
    
2. Estampillez chaque appel à [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md). 
    
3. Évaluez s'il est nécessaire ou non d'effectuer une mise à jour complète en fonction de la durée écoulée depuis le dernier appel. Si une mise à jour complète est nécessaire, appelez **IMAPISupport:: OpenTemplateID** avec l'indicateur FILL_ENTRY. Si ce n'est pas nécessaire, ne définissez pas l'indicateur sur l'appel. 
    
Lorsqu'un client envoie une demande pour l'une des propriétés du destinataire copié, votre fournisseur peut choisir de gérer la demande lui-même ou d'utiliser le code fourni par le fournisseur étranger. Votre fournisseur peut s'attendre à ce que le fournisseur étranger intercepte la plupart des appels à **IMAPIProp** , à l'exception de [IMAPIProp:: OpenProperty](imapiprop-openproperty.md). Un appel à **OpenProperty** qui demande la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) est toujours transféré à votre fournisseur.
  
 **Pour accéder au code d'identificateur de modèle**
  
1. Ouvrez le destinataire et appelez sa méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) pour récupérer la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Si **GetProps** échoue car **PR_TEMPLATEID** n'est pas disponible, le fournisseur étranger ne prend pas en charge un identificateur de modèle et le code associé pour ce destinataire. Votre fournisseur doit utiliser son implémentation du destinataire pour toutes les opérations de maintenance. 
    
2. Si l'identificateur de modèle est renvoyé depuis **GetProps**, transmettez-le et un pointeur vers l'implémentation **IMAPIProp** du destinataire dans un appel à la méthode **IMAPISupport:: OpenTemplateID** . Définissez l'indicateur FILL_ENTRY si la plupart ou la totalité des propriétés du destinataire doivent être mises à jour, par exemple lors de la création ou si elles n'ont pas été mises à jour pendant un certain temps. 
    
3. Si **OpenTemplateID** renvoie l'implémentation **IMAPIProp** du fournisseur étranger, revenez au client un pointeur vers cette implémentation. 
    
4. Si **OpenTemplateID** ne retourne pas d'implémentation, généralement parce que le fournisseur étranger n'est pas dans le profil, revenez au client un pointeur vers l'implémentation de **IMAPIProp** de votre fournisseur. Le client doit pouvoir utiliser les propriétés de l'objet à l'aide de l'une ou l'autre des interfaces. 
    

