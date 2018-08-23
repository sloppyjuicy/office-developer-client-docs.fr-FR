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
ms.openlocfilehash: d5b2aa2830e2721b9f895b22df12c9d712188625
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590133"
---
# <a name="adding-address-book-entries"></a>Ajout d’entrées de carnet d’adresses

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour ajouter un utilisateur de messagerie ou une liste de distribution à un conteneur ou d’un fournisseur, un client appelle [IAddrBook::NewEntry](iaddrbook-newentry.md) appelle [IMAPISupport::NewEntry](imapisupport-newentry.md) avec l’identificateur d’entrée du conteneur cible dans le paramètre _lpEIDContainer_ . MAPI appelle ensuite la méthode de [IABContainer::CreateEntry](iabcontainer-createentry.md) du conteneur pour créer l’entrée à l’aide d’un modèle unique d’une table unique. Un modèle unique autorise le client à créer un nouveau destinataire d’un type particulier. La plupart des champs sont modifiable. Le modèle indiqué par le paramètre _lpEntryID_ peut être une que fournit votre fournisseur ou il peut être un modèle à partir d’un fournisseur externe, si votre fournisseur prend en charge les modèles étrangères. Les implémentations de **CreateEntry** pour les fournisseurs qui peuvent créer des destinataires à partir d’un modèle étrangère sont toujours plus complexe que pour les fournisseurs qui ne peuvent pas les implémentations. 
  
 **Pour mettre en œuvre IABContainer::CreateEntry**
  
1. Déterminer le type d’identificateur d’entrée spécifié par le paramètre _lpEntryID_ . 
    
2. Si l’identificateur d’entrée représente un modèle pour un utilisateur de messagerie, une liste de distribution ou un conteneur de carnet d’adresses appartenant à votre fournisseur de :
    
1. Créer et initialiser l’objet approprié. Votre fournisseur peut définir certaines propriétés initiales si vous le souhaitez. Ces propriétés dépendent du type de destinataire en cours de création. 
    
2. Retourne un pointeur vers l’implémentation de l’objet dans le contenu du paramètre _lppMAPIPropEntry_ . 
    
3. Si l’identificateur d’entrée représente un modèle pour un fournisseur externe :
    
1. Appelez [IMAPISupport::OpenEntry](imapisupport-openentry.md) pour ouvrir l’objet étranger. 
    
2. Appelez la méthode l’objet [IMAPIProp::GetProps](imapiprop-getprops.md) , en passant NULL pour le tableau de balise de propriété, pour récupérer ses propriétés. 
    
3. Modifier le tableau de valeurs de propriété renvoyé par **GetProps** en modifiant la balise de propriété pour PR_NULL pour toutes les propriétés qui ne s’applique pas au nouvel objet et ne doivent pas être transférées. 
    
4. Créez un identificateur d’entrée pour le nouvel objet. 
    
5. Créer un nouvel objet de la saisie, soit messagerie utilisateur ou liste de distribution.
    
6. Initialiser le nouvel objet en définissant les propriétés par défaut.
    
7. Vérifier si l’objet étrangère prend en charge la propriété **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). 
    
8. Si l’objet étrangère prend en charge **PR_TEMPLATEID**, appelez [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) pour récupérer une interface d’objet de propriété à partir du fournisseur étranger et définir le contenu du paramètre _lppMAPIPropEntry_ à la propriété étrangère implémentation de l’objet. 
    
9. Si l’objet étranger ne gère pas **PR_TEMPLATEID**, définissez le contenu du paramètre _lppMAPIPropEntry_ pour l’implémentation de votre fournisseur du nouvel objet. 
    
10. Appelez la méthode [IMAPIProp::SetProps](imapiprop-setprops.md) de l’objet désigné par le paramètre _lppMAPIPropEntry_ pour définir les propriétés appropriées de l’objet étranger. 
    

