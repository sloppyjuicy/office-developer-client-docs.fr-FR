---
title: Copie des entrées du carnet d’adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: e795bbd5b521abc8c2a6cc7bb9e8fc59e6d22844
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62781568"
---
# <a name="copying-address-book-entries"></a>Copie des entrées du carnet d’adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La méthode [IABContainer::CopyEntries](iabcontainer-copyentries.md) de votre conteneur est appelée lorsqu’un ou plusieurs destinataires du même conteneur ou d’un autre conteneur doivent être copiés dans ce conteneur. **CopyEntries** possède quatre paramètres d’entrée : un tableau d’identificateurs d’entrée représentant les destinataires à copier, une poignée de fenêtre pour l’indicateur de progression, un pointeur d’objet de progression et une valeur d’indicateurs. Votre fournisseur doit afficher la progression si l’indicateur AB_NO_DIALOG n’est pas définie et utiliser l’objet de progression du paramètre  _lpProgress_ s’il n’est pas NULL. Si  _lpProgress_ est NULL, appelez [IMAPISupport::D oProgressDialog](imapisupport-doprogressdialog.md) pour utiliser l’objet de progression MAPI. Pour plus d’informations sur l’affichage de la progression, voir [Affichage d’un indicateur de progression](mapi-progress-indicators.md).
  
En plus de AB_NO_DIALOG supprimer un indicateur de progression, l’un des deux autres indicateurs peut être définie pour demander un type de vérification des entrées en double : CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT. Les indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT sont uniquement des suggestions quant à la façon dont votre fournisseur détermine les entrées en double et peut être ignorée. MAPI suggère à votre fournisseur d’implémenter la prise en charge de ces indicateurs comme suit.
  
|**Indicateur d’entrée en double**|**Implémentation suggérée**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Vérifiez si le nom complet de l’entrée à créer correspond au nom complet d’une entrée déjà dans le conteneur. |
|CREATE_CHECK_DUP_STRICT  <br/> |Vérifiez si le nom complet et la clé de recherche dans l’entrée à créer correspondent au nom d’affichage et à la clé de recherche d’une entrée de conteneur. |
   
Le dernier indicateur, CREATE_REPLACE, indique que la nouvelle entrée doit remplacer l’entrée existante si votre fournisseur a déterminé qu’une entrée à créer est un doublon d’une entrée déjà dans votre conteneur. 
  
Si votre fournisseur est un carnet d’adresses personnel, incluez la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) dans chaque opération de copie. Inclure le tableau d’affichage des détails d’un destinataire copié permet à votre conteneur d’afficher les détails du destinataire au lieu d’appeler le conteneur d’origine pour créer l’affichage.
  
 **Pour implémenter IABContainer::CopyEntries**
  
1. Déterminez si chaque identificateur d’entrée dans le paramètre _lpEntries_ est dans un format géré par votre fournisseur et, si ce n’est pas le cas, échouez et renvoyez MAPI_E_INVALID_ENTRYID. 
    
2. Si un identificateur d’entrée représente un utilisateur de messagerie, une liste de distribution ou un conteneur géré par votre fournisseur :
    
1. Appelez votre [méthode IMAPISupport::OpenEntry](imapisupport-openentry.md) pour ouvrir le destinataire correspondant. 
    
2. Copiez le destinataire dans votre conteneur. 
    
3. Si l’identificateur d’entrée représente un destinataire étranger :
    
1. Appelez la méthode [IABContainer::CreateEntry](iabcontainer-createentry.md) de votre conteneur pour créer un destinataire. 
    
2. Définissez les propriétés initiales sur le nouveau destinataire.
    
4. Appelez la méthode [IMAPIProp::SaveChanges](imapiprop-savechanges.md) du nouvel objet pour l’enregistrer. 
    
5. Mettez à jour la table des matières du conteneur pour refléter le nouveau destinataire. 
    
6. [Appelez IMAPISupport::Notify](imapisupport-notify.md) pour envoyer une notification de table aux clients inscrits. 
    

