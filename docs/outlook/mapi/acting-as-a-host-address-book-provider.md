---
title: Rôle de fournisseur de carnet d’adresses hôte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f06a1034-ee49-4a09-831e-9752713228a8
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: de0acb88eee6addc0347f5281e5fbe5070bad0a4
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595406"
---
# <a name="acting-as-a-host-address-book-provider"></a>Rôle de fournisseur de carnet d’adresses hôte

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Un fournisseur d’hébergement est un fournisseur de carnet d’adresses qui inclut les destinataires à partir d’autres fournisseurs dans ses conteneurs et s’appuie sur l’implémentation des destinataires par les autres fournisseurs partiellement contrôler leur maintenance. Un fournisseur d’hébergement utilise les identificateurs de modèle de ces destinataires étrangers pour lier les données pour ces destinataires au code dans le fournisseur étranger. Ce processus de liaison est déclenché lorsque votre fournisseur récupère la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) d’un destinataire et lui passe un appel à [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
  
Lors de vos appels fournisseur **IMAPISupport::OpenTemplateID**, MAPI établit une correspondance avec la **MAPIUID** au sein de l’identificateur de modèle avec une **MAPIUID** enregistré par un fournisseur et appelle la méthode du fournisseur [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) . Le fournisseur étranger peut retourner un pointeur à l’objet de propriété de votre fournisseur, à sa propre implémentation d’objet de propriété, ou à une implémentation qui encapsule votre objet de fournisseur. Le pointeur retourné est placé dans le contenu du paramètre _lppMAPIPropNew_ . 
  
Votre fournisseur de la possibilité d’appeler **IMAPISupport::OpenTemplateID** avec l’indicateur FILL_ENTRY défini ou non. Définissez cet indicateur lorsque le destinataire est créé ou lorsque le temps écoulé depuis votre fournisseur a mis à jour les propriétés du destinataire. Une utilisation courante de l’indicateur FILL_ENTRY consiste à conserver un destinataire dans votre fournisseur synchronisé avec l’original. L’implémentation de ce type de planification de la synchronisation améliore les performances. 
  
 **Pour conserver un destinataire externe synchronisé**
  
1. Déterminez un intervalle approprié pour les mises à jour périodiques. 
    
2. Horodatage pour chaque appel à [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md). 
    
3. Évaluez si elle est nécessaire effectuer une mise à jour complète en fonction de la quantité de temps a expiré depuis le dernier appel ou non. Si une mise à jour complète est nécessaire, appelez **IMAPISupport::OpenTemplateID** avec l’indicateur FILL_ENTRY. Si elle n’est pas nécessaire, ne définissez pas l’indicateur de l’appel. 
    
Lorsqu’un client émet une demande d’une des propriétés du destinataire copié, votre fournisseur peut choisir de traiter la demande elle-même ou utilisez le code fourni par le fournisseur étranger. Votre fournisseur de prévoir le fournisseur étranger pour intercepter plus, dans le cas contraire, les appels vers **IMAPIProp** à l’exception de [IMAPIProp::OpenProperty](imapiprop-openproperty.md). Un appel à **OpenProperty** demande la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) est toujours transféré à votre fournisseur.
  
 **Pour accéder au code d’identificateur de modèle**
  
1. Ouvrez le destinataire et appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) pour récupérer la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Si **GetProps** échoue car **PR_TEMPLATEID** n’est pas disponible, le fournisseur étranger ne gère pas un identificateur de modèle et le code pour ce destinataire. Votre fournisseur devra utiliser son implémentation du destinataire pour la maintenance de tous les. 
    
2. Si l’identificateur de modèle est renvoyé à partir de **GetProps**, transmettez et un pointeur à l’implémentation de **IMAPIProp** du destinataire dans un appel à la méthode **IMAPISupport::OpenTemplateID** . Définir l’indicateur FILL_ENTRY si tout ou partie des propriétés du destinataire doivent être mis à jour, par exemple au moment de la création ou si elles n'ont pas été mis à jour pendant un certain temps. 
    
3. Si **OpenTemplateID** renvoie l’étranger implémentation du fournisseur **IMAPIProp** , retourne un pointeur vers cette implémentation au client. 
    
4. Si **OpenTemplateID** ne retourne pas d’une implémentation, généralement car le fournisseur étranger n’est pas dans le profil, renvoie au client un pointeur vers l’implémentation de votre fournisseur **IMAPIProp** . Le client doit être en mesure d’utiliser les propriétés de l’objet à l’aide de l’interface. 
    

