---
title: Implémentation des tables d'affichage
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339948"
---
# <a name="display-table-implementation"></a>Implémentation des tables d'affichage

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une table d'affichage est utilisée pour afficher une feuille de propriétés, une boîte de dialogue spéciale constituée d'une ou de plusieurs pages de propriétés à onglets dédiées à l'affichage et éventuellement la modification d'une ou plusieurs propriétés. L'implémentation de l'interface [IAttach: IMAPIProp](iattachimapiprop.md) est associée à chaque table d'affichage. L'implémentation de [IMAPIProp](imapipropiunknown.md) gère les données de propriété présentées dans la feuille des propriétés. 
  
Les lignes d'une table d'affichage représentent les contrôles de la feuille des propriétés. La plupart des contrôles peuvent être associés à des propriétés gérées à l'aide de l'implémentation **IMAPIProp** . Lorsqu'un utilisateur modifie la valeur d'un contrôle modifiable, la propriété correspondante est mise à jour. 
  
Les colonnes d'une table d'affichage représentent les propriétés du contrôle, telles que sa position dans la feuille des propriétés, son type, sa structure associée et son identificateur. Pour obtenir la liste complète des colonnes de tableau d'affichage requises, consultez la rubrique [Display tables](display-tables.md).
  
MAPI affiche une feuille de propriétés à l'utilisateur d'une application cliente en lisant les valeurs des propriétés de l'implémentation **IMAPIProp** associée à la table d'affichage ou à partir de la table d'affichage directement. Lorsque l'utilisateur travaille sur la feuille des propriétés, en modifiant les valeurs dans les contrôles, MAPI appelle [IMAPIProp:: SetProps](imapiprop-setprops.md) pour enregistrer un contrôle modifié si l'indicateur DT_SET_IMMEDIATE du contrôle est défini. Pour les contrôles sans l'indicateur DT_SET_IMMEDIATE, les modifications apportées aux propriétés sont enregistrées lorsque l'utilisateur fait disparaître la boîte de dialogue en cliquant sur le bouton **OK** ou **appliquer maintenant** . Lorsque l'utilisateur clique sur l'un ou l'autre de ces boutons ou sur le bouton **Annuler** , MAPI supprime la feuille de propriétés de l'affichage. 
  
MAPI accède à votre table d'affichage en appelant la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) dans l'implémentation **IMAPIProp** et en demandant la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) ou en l'héritant d'un appel que vous avez effectué vers MAPI, tel que [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md).
  
La première technique d'accès est utilisée lorsque des fournisseurs de carnet d'adresses sont invités à afficher des détails sur les utilisateurs de messagerie ou les listes de distribution. Le traitement suivant se produit:
  
1. Un client appelle la méthode [IAddrBook::D etails](iaddrbook-details.md) . 
    
2. MAPI appelle la méthode [IABLogon:: OpenEntry](iablogon-openentry.md) du fournisseur de carnet d'adresses pour accéder à l'utilisateur de messagerie qui représente l'entrée sélectionnée. 
    
3. MAPI appelle la méthode [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) de l'utilisateur de messagerie pour récupérer la propriété **PR_DETAILS_TABLE** , la table d'affichage de la boîte de dialogue détails. 
    
4. MAPI affiche la boîte de dialogue, qui gère l'interaction de l'utilisateur avec les informations, et la supprime lorsque l'utilisateur a terminé. 
    
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

