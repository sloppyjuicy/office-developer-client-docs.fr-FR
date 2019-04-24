---
title: Copie d'entrées de carnet d'adresses
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 285abeb4-45c8-4e82-9a16-b935b4651afe
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 190c4bf12c8f5aaaf8143f59239bb53fb68046f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32333067"
---
# <a name="copying-address-book-entries"></a>Copie d'entrées de carnet d'adresses

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
La méthode [IABContainer:: CopyEntries](iabcontainer-copyentries.md) de votre conteneur est appelée lorsqu'un ou plusieurs destinataires du même conteneur ou d'un autre conteneur doivent être copiés dans ce conteneur. **CopyEntries** comporte quatre paramètres d'entrée: un tableau d'identificateurs d'entrée représentant les destinataires à copier, un handle de fenêtre pour l'indicateur de progression, un pointeur d'objet de progression et une valeur d'indicateurs. Votre fournisseur doit afficher la progression si l'indicateur AB_NO_DIALOG n'est pas défini et utiliser l'objet Progress à partir du paramètre _lpProgress_ s'il n'est pas null. Si _lpProgress_ est null, appelez [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) pour utiliser l'objet de progression MAPI. Pour plus d'informations sur l'affichage de la progression, voir [affichage d'un indicateur de progression](mapi-progress-indicators.md).
  
En plus de AB_NO_DIALOG pour supprimer un indicateur de progression, un des deux autres indicateurs peut être défini pour demander un type de vérification d'entrées en double: CREATE_CHECK_DUP_LOOSE ou CREATE_CHECK_DUP_STRICT. Les indicateurs CREATE_CHECK_DUP_LOOSE et CREATE_CHECK_DUP_STRICT ne sont que des suggestions quant à la façon dont votre fournisseur détermine les entrées en double et peut être ignoré. MAPI suggère que votre fournisseur implémente la prise en charge de ces indicateurs comme suit.
  
|**Indicateur d'entrée en double**|**Implémentation suggérée**|
|:-----|:-----|
|CREATE_CHECK_DUP_LOOSE  <br/> |Vérifiez si le nom complet dans l'entrée à créer correspond au nom complet d'une entrée qui se trouve déjà dans le conteneur.  <br/> |
|CREATE_CHECK_DUP_STRICT  <br/> |Vérifiez si le nom complet et la clé de recherche dans l'entrée à créer correspondent au nom complet et à la clé de recherche d'une entrée de conteneur.  <br/> |
   
Le dernier indicateur, CREATE_REPLACE, indique que la nouvelle entrée doit remplacer celle existante si votre fournisseur a déterminé qu'une entrée à créer est un doublon d'une entrée se trouvant déjà dans votre conteneur. 
  
Si votre fournisseur est un carnet d'adresses personnel, incluez la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) dans chaque opération de copie. L'inclusion de la table d'affichage des détails d'un destinataire copié permet à votre conteneur d'afficher les détails du destinataire au lieu d'appeler le conteneur d'origine pour créer l'affichage.
  
 **Pour implémenter IABContainer:: CopyEntries**
  
1. Déterminez si chaque identificateur d'entrée dans le paramètre _lpEntries_ est dans un format que votre fournisseur gère et, si ce n'est pas le cas, échoue et renvoie MAPI_E_INVALID_ENTRYID. 
    
2. Si un identificateur d'entrée représente un utilisateur de messagerie, une liste de distribution ou un conteneur géré par votre fournisseur:
    
1. Appelez la méthode [IMAPISupport:: OpenEntry](imapisupport-openentry.md) pour ouvrir le destinataire correspondant. 
    
2. Copiez le destinataire dans votre conteneur. 
    
3. Si l'identificateur d'entrée représente un destinataire étranger:
    
1. Appelez la méthode [IABContainer:: CreateEntry](iabcontainer-createentry.md) de votre conteneur pour créer un destinataire. 
    
2. Définissez les propriétés initiales du nouveau destinataire.
    
4. Appelez la méthode [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) de l'objet pour l'enregistrer. 
    
5. Mettez à jour la table des matières du conteneur pour refléter le nouveau destinataire. 
    
6. Appeler [IMAPISupport:: Notify](imapisupport-notify.md) pour envoyer une notification de table aux clients inscrits. 
    

