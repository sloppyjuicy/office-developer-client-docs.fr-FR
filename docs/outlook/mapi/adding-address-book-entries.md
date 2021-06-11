---
title: Ajout d’entrées de carnet d’adresses
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63444a65-d56a-4dbd-9aa6-e60f18ba8104
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 8dc82a99ee088d42c076ca9a3a75eac6553f7d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421339"
---
# <a name="adding-address-book-entries"></a>Ajout d’entrées de carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour ajouter un utilisateur de messagerie ou une liste de distribution à un conteneur, un client appelle [IAddrBook::NewEntry](iaddrbook-newentry.md) ou un fournisseur appelle [IMAPISupport::NewEntry](imapisupport-newentry.md) avec l’identificateur d’entrée du conteneur cible dans le paramètre _lpEIDContainer._ MAPI appelle à son tour la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) du conteneur pour créer l’entrée à l’aide d’un modèle unique à partir d’une table unique. Un modèle unique permet au client de créer un destinataire d’un type particulier. La plupart des champs sont modifiables. Le modèle pointé par le paramètre  _lpEntryID_ peut être celui que votre fournisseur fournit ou il peut s’agit d’un modèle provenant d’un fournisseur étranger, si votre fournisseur prend en charge les modèles étrangers. Les implémentations **de CreateEntry** pour les fournisseurs qui peuvent créer des destinataires à partir d’un modèle étranger sont toujours plus complexes que les implémentations pour les fournisseurs qui ne le peuvent pas. 
  
 **Pour implémenter IABContainer::CreateEntry**
  
1. Déterminez le type d’identificateur d’entrée spécifié par _le paramètre lpEntryID._ 
    
2. Si l’identificateur d’entrée représente un modèle pour un utilisateur de messagerie, une liste de distribution ou un conteneur de carnet d’adresses qui appartient à votre fournisseur :
    
1. Créer et initialiser l’objet approprié. Votre fournisseur peut définir certaines propriétés initiales si vous le souhaitez. Ces propriétés dépendent du type de destinataire créé. 
    
2. Renvoyer un pointeur vers l’implémentation de l’objet dans le contenu du _paramètre lppMAPIPropEntry._ 
    
3. Si l’identificateur d’entrée représente un modèle pour un fournisseur étranger :
    
1. Appelez [IMAPISupport::OpenEntry](imapisupport-openentry.md) pour ouvrir l’objet étranger. 
    
2. Appelez la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) de l’objet, en passant NULL pour le tableau de balises de propriétés, pour récupérer ses propriétés. 
    
3. Modifiez le tableau de valeurs de propriétés renvoyé par **GetProps** en modifiant la balise de propriété en PR_NULL pour toutes les propriétés qui ne s’appliquent pas au nouvel objet et ne doivent pas être transférées. 
    
4. Créez un identificateur d’entrée pour le nouvel objet. 
    
5. Créez un objet du type approprié, utilisateur de messagerie ou liste de distribution.
    
6. Initialise le nouvel objet en dérisant les propriétés par défaut.
    
7. Vérifiez si l’objet étranger prend en **charge la PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). 
    
8. Si l’objet étranger prend en charge **PR_TEMPLATEID**, appelez [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) pour récupérer une interface d’objet de propriété auprès du fournisseur étranger et définissez le contenu du paramètre  _lppMAPIPropEntry_ sur l’implémentation de l’objet de propriété étrangère. 
    
9. Si l’objet étranger ne prend **pas en charge PR_TEMPLATEID**, définissez le contenu du paramètre  _lppMAPIPropEntry_ sur l’implémentation du nouvel objet par votre fournisseur. 
    
10. Appelez la [méthode IMAPIProp::SetProps](imapiprop-setprops.md) de l’objet pointé par le paramètre  _lppMAPIPropEntry_ pour définir les propriétés appropriées à partir de l’objet étranger. 
    

