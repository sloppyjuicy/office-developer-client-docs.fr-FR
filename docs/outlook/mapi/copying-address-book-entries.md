---
title: Copie les entrées de carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ce7f7e2db341be62912935b7a55d69eaf5db8ab5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783074"
---
# <a name="copying-address-book-entries"></a>Copie les entrées de carnet d’adresses

  
  
**S’applique à**: Outlook 
  
Méthode de [IABContainer::CopyEntries](iabcontainer-copyentries.md) de votre conteneur est appelée lorsque un ou plusieurs destinataires à partir du même ou un autre conteneur doivent être copiés dans ce conteneur. **CopyEntries** comporte quatre paramètres d’entrée : un tableau d’identificateurs d’entrée représentant les destinataires à copier, un handle de fenêtre pour l’indicateur de progression, un pointeur d’objet de progression et une valeur pour les indicateurs. Votre fournisseur doit afficher la progression si l’indicateur AB_NO_DIALOG n’est pas défini et que vous utilisez l’objet de l’avancement du paramètre _lpProgress_ si elle n’est pas NULL. Si _lpProgress_ est NULL, appelez [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) pour utiliser l’objet de l’avancement MAPI. Pour plus d’informations sur l’affichage de la progression, voir [affichant un indicateur de progression](mapi-progress-indicators.md).
  
Outre AB_NO_DIALOG pour supprimer un indicateur de progression, une des deux autres indicateurs peut être définie pour demander un type de vérification de l’entrée en double : CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT. Les indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT sont uniquement des suggestions quant au comment votre fournisseur détermine les entrées en double et peuvent être ignorés. MAPI suggère que votre fournisseur de mettre en œuvre la prise en charge pour ces indicateurs comme suit.
  
|**Indicateur d’entrée en double**|**Implémentation suggérée**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Vérifiez si le nom complet de l’entrée à créer correspond au nom de l’affichage d’une entrée déjà dans le conteneur.  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |Vérifiez si le nom complet et la clé de recherche dans l’entrée doit être créé correspondent à la clé de recherche et le nom complet d’une entrée de conteneur.  <br/> |
   
Le dernier indicateur, CREATE_REPLACE, indique que la nouvelle entrée doit remplacer ce dernier si votre fournisseur a déterminé qu’une entrée à créer une copie d’une entrée déjà dans le conteneur. 
  
Si votre fournisseur est un carnet d’adresses personnel, inclure la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) dans chaque opération de copie. Y compris la table d’affichage Détails d’un destinataire copié permet de votre conteneur afficher les détails du destinataire au lieu d’avoir à appeler le conteneur d’origine pour créer l’affichage.
  
 **Pour mettre en œuvre IABContainer::CopyEntries**
  
1. Déterminer si chaque identificateur d’entrée dans le paramètre _lpEntries_ est dans un format qui gère votre fournisseur et si elle n’est pas, échouer et retourner MAPI_E_INVALID_ENTRYID. 
    
2. Si un identificateur d’entrée représente un utilisateur de messagerie, une liste de distribution ou un conteneur qui gère votre fournisseur :
    
1. Appeler votre méthode [IMAPISupport::OpenEntry](imapisupport-openentry.md) pour ouvrir le destinataire correspondant. 
    
2. Copiez le destinataire dans votre conteneur. 
    
3. Si l’identificateur d’entrée représente un destinataire externe :
    
1. Appelez la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) de votre conteneur pour créer un nouveau destinataire. 
    
2. Définir les propriétés initiales sur le nouveau destinataire.
    
4. Appeler la nouvelle méthode l’objet [IMAPIProp::SaveChanges](imapiprop-savechanges.md) pour l’enregistrer. 
    
5. Mettre à jour la table de contenu du conteneur pour refléter le nouveau destinataire. 
    
6. Appelez [IMAPISupport::Notify](imapisupport-notify.md) pour envoyer une notification de la table aux clients enregistrés. 
    

