---
title: Implémentation du tableau d’affichage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
ms.openlocfilehash: d6637bf77a7579dab0d2bbf25451635f557ad6fa
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63375047"
---
# <a name="display-table-implementation"></a>Implémentation du tableau d’affichage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Un tableau d’affichage est utilisé pour afficher une feuille des propriétés, une boîte de dialogue spéciale composée d’une ou plusieurs pages de propriétés à onglets dédiées à l’affichage et éventuellement à la modification d’une ou de plusieurs propriétés. Une implémentation d’interface [IAttach : IMAPIProp](iattachimapiprop.md) est associée à chaque tableau d’affichage. [L’implémentation IMAPIProp](imapipropiunknown.md) conserve les données de propriété présentées dans la feuille des propriétés. 
  
Les lignes d’un tableau d’affichage représentent les contrôles de la feuille des propriétés. La plupart des contrôles peuvent être associés à des propriétés conservées avec **l’implémentation IMAPIProp** . Lorsqu’un utilisateur modifie la valeur d’un contrôle modifiable, la propriété correspondante est mise à jour. 
  
Les colonnes d’un tableau d’affichage représentent les propriétés du contrôle, telles que sa position dans la feuille des propriétés, son type, la structure associée et l’identificateur. Pour obtenir la liste complète des colonnes de tableau d’affichage requises, voir [Tableaux d’affichage](display-tables.md).
  
MAPI affiche une feuille de propriétés à l’utilisateur d’une application cliente en lisant les valeurs des propriétés à partir de l’implémentation **IMAPIProp** associée au tableau d’affichage ou directement à partir du tableau d’affichage. Lorsque l’utilisateur travaille avec la feuille des propriétés, en modifiant les valeurs dans les contrôles, MAPI appelle [IMAPIProp::SetProps](imapiprop-setprops.md) pour enregistrer un contrôle modifié si l’indicateur DT_SET_IMMEDIATE du contrôle est définie. Pour les contrôles sans l’indicateur DT_SET_IMMEDIATE, les modifications apportées aux propriétés sont enregistrées lorsque l’utilisateur fait disparaître la boîte de dialogue en cliquant sur le bouton **OK** ou Appliquer **maintenant** . Lorsque vous cliquez sur l’un  de ces boutons ou sur le bouton Annuler, MAPI supprime la feuille des propriétés de l’affichage. 
  
MAPI accède à votre table d’affichage en appelant la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) dans l’implémentation **IMAPIProp** et en demandant la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) ou en l’héritant dans un appel que vous avez effectué à MAPI, tel que [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md).
  
La première technique d’accès est utilisée lorsque les fournisseurs de carnets d’adresses sont invités à afficher des détails sur les utilisateurs de messagerie ou les listes de distribution. Le traitement suivant se produit :
  
1. Un client appelle [la méthode IAddrBook::D etails](iaddrbook-details.md) . 
    
2. MAPI appelle la méthode [IABLogon::OpenEntry](iablogon-openentry.md) du fournisseur de carnet d’adresses pour accéder à l’utilisateur de messagerie qui représente l’entrée sélectionnée. 
    
3. MAPI appelle la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de l’utilisateur de messagerie pour récupérer la propriété **PR_DETAILS_TABLE** , le tableau d’affichage de la boîte de dialogue détails. 
    
4. MAPI affiche la boîte de dialogue, qui gère l’interaction de l’utilisateur avec les informations et les supprime lorsque l’utilisateur a terminé. 
    
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

