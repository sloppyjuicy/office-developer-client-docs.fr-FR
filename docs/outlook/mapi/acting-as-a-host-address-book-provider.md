---
title: Agir en tant que fournisseur de carnet d’adresses hôte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 202d4b4391de7553e39e50dc527df5502ebcefb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406464"
---
# <a name="acting-as-a-host-address-book-provider"></a>Agir en tant que fournisseur de carnet d’adresses hôte

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un fournisseur d’hôte est un fournisseur de carnet d’adresses qui inclut des destinataires d’autres fournisseurs dans ses conteneurs et s’appuie sur l’implémentation des destinataires par les autres fournisseurs pour contrôler partiellement leur maintenance. Un fournisseur d’hôte utilise les identificateurs de modèle de ces destinataires étrangers pour lier les données de ces destinataires au code dans le fournisseur étranger. Ce processus de liaison est initié lorsque votre fournisseur récupère la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) d’un destinataire et la transmet dans un appel à [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
  
Lorsque votre fournisseur appelle **IMAPISupport::OpenTemplateID,** MAPI correspond au **MAPIUID** dans l’identificateur de modèle avec un **MAPIUID** enregistré par un fournisseur et appelle la méthode [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) du fournisseur. Le fournisseur étranger peut renvoyer un pointeur vers l’objet de propriété de votre fournisseur, vers sa propre implémentation d’objet de propriété ou vers une implémentation qui encapsule l’objet de votre fournisseur. Le pointeur renvoyé est placé dans le contenu du _paramètre lppMAPIPropNew._ 
  
Votre fournisseur peut choisir d’appeler ou non **IMAPISupport::OpenTemplateID** avec l’indicateur FILL_ENTRY définie. Définissez cet indicateur lorsque le destinataire est créé ou qu’un certain temps s’est écoulé depuis que votre fournisseur a actualisé les propriétés du destinataire. Une utilisation courante de l’indicateur FILL_ENTRY est de maintenir un destinataire dans votre fournisseur synchronisé avec l’original. L’implémentation de ce type de planification de synchronisation améliore les performances. 
  
 **Pour maintenir la synchronisation d’un destinataire étranger**
  
1. Déterminez un intervalle approprié pour les mises à jour périodiques. 
    
2. Timestamp each call to [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
    
3. Évaluez s’il est nécessaire d’effectuer une mise à jour complète en fonction de la durée écoulée depuis le dernier appel. Si une mise à jour complète est nécessaire, appelez **IMAPISupport::OpenTemplateID** avec l’indicateur FILL_ENTRY’appel. Si ce n’est pas nécessaire, ne définissez pas l’indicateur sur l’appel. 
    
Lorsqu’un client effectue une demande pour l’une des propriétés du destinataire copié, votre fournisseur peut choisir de gérer la demande elle-même ou d’utiliser le code fourni par le fournisseur étranger. Votre fournisseur peut s’attendre à ce que le fournisseur étranger intercepte la plupart, sinon la totalité, des appels vers **IMAPIProp,** à l’exception de [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Un appel à **OpenProperty** demandant la **propriété PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) est toujours transmis à votre fournisseur.
  
 **Pour accéder au code d’identificateur du modèle**
  
1. Ouvrez le destinataire et appelez sa méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer la PR_TEMPLATEID **(** [PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Si **GetProps échoue** parce **PR_TEMPLATEID** est indisponible, le fournisseur étranger ne prend pas en charge l’identificateur de modèle et le code associé pour ce destinataire. Votre fournisseur devra utiliser son implémentation du destinataire pour toutes les opérations de maintenance. 
    
2. Si l’identificateur de modèle est renvoyé par **GetProps,** passez-le et un pointeur vers l’implémentation **IMAPIProp** du destinataire dans un appel à la méthode **IMAPISupport::OpenTemplateID.** Définissez l’indicateur FILL_ENTRY si la plupart ou l’ensemble des propriétés du destinataire doivent être mises à jour, par exemple au moment de la création ou si elles n’ont pas été mises à jour pendant un certain temps. 
    
3. Si **OpenTemplateID** renvoie l’implémentation **IMAPIProp** du fournisseur étranger, retournez au client un pointeur vers cette implémentation. 
    
4. Si **OpenTemplateID** ne retourne pas d’implémentation, généralement parce que le fournisseur étranger ne se trouve pas dans le profil, renvoyez au client un pointeur vers l’implémentation **IMAPIProp** de votre fournisseur. Le client doit pouvoir utiliser les propriétés de l’objet à l’aide de l’une ou l’autre interface. 
    

