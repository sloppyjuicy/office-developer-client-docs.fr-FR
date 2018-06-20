---
title: Affichage tableau implémentation
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 07ad94c423c3be425dc905dc578f55ad2c467a95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783167"
---
# <a name="display-table-implementation"></a>Affichage tableau implémentation

  
  
**S’applique à**: Outlook 
  
Un tableau d’affichage est utilisé pour afficher une feuille de propriétés, une boîte de dialogue se compose d’une ou plusieurs pages de propriétés dédiée à afficher et de modifier éventuellement une ou plusieurs propriétés. Associé à chaque table est un [IAttach : IMAPIProp](iattachimapiprop.md) implémentation de l’interface. L’implémentation [IMAPIProp](imapipropiunknown.md) gère les données de propriété qui sont présentées dans la feuille des propriétés. 
  
Les lignes dans un affichage de tableau représentent les contrôles dans la feuille des propriétés. La plupart des contrôles peut être associé à des propriétés gérées avec l’implémentation **IMAPIProp** . Lorsqu’un utilisateur modifie la valeur d’un contrôle modifiable, la propriété correspondante est mis à jour. 
  
Les colonnes dans un affichage de tableau représentent les propriétés du contrôle, telles que sa position dans la feuille des propriétés, son type, structure associée et identificateur. Pour obtenir une liste complète des colonnes de tableau d’affichage requis, voir [Afficher les Tables](display-tables.md).
  
MAPI affiche une feuille de propriétés à l’utilisateur d’une application cliente en lisant les valeurs de propriété à partir de l’implémentation **IMAPIProp** associé à la table d’affichage ou de la table d’affichage directement. Lorsque l’utilisateur avec la feuille des propriétés, modification des valeurs dans les contrôles, appels MAPI [IMAPIProp::SetProps](imapiprop-setprops.md) pour enregistrer un contrôle modifié si l’indicateur de DT_SET_IMMEDIATE du contrôle est défini. Pour les contrôles sans l’indicateur DT_SET_IMMEDIATE est défini, les modifications apportées aux propriétés sont enregistrées lorsque l’utilisateur ferme la boîte de dialogue en cliquant sur le bouton **OK** ou **Appliquer** . Un clic sur un de ces boutons ou sur le bouton **Annuler** , MAPI supprime la feuille des propriétés d’affichage. 
  
MAPI accède à la table d’affichage en appelant la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) dans l’implémentation **IMAPIProp** et demande la propriété **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) ou par héritage dans un appel que vous avez apportées à MAPI, tel que [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).
  
La première technique d’accès est utilisée lorsque les fournisseurs de carnet d’adresses sont invités à afficher plus d’informations sur les utilisateurs ou les listes de distribution de messagerie. Le traitement suivant se produit :
  
1. Un client appelle la méthode [IAddrBook::Details](iaddrbook-details.md) . 
    
2. MAPI appelle la méthode de [IABLogon::OpenEntry](iablogon-openentry.md) du fournisseur de carnet d’adresses pour accéder à l’utilisateur de messagerie qui représente l’entrée sélectionnée. 
    
3. MAPI appelle la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de l’utilisateur de messagerie pour récupérer la propriété **PR_DETAILS_TABLE** , la table d’affichage de la boîte de dialogue Détails. 
    
4. MAPI affiche la boîte de dialogue Gestion de l’interaction avec les informations de l’utilisateur et le supprime lorsque l’utilisateur est terminée. 
    
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)

