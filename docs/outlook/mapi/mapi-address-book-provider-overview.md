---
title: Vue d’ensemble du fournisseur de carnet d’adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
ms.openlocfilehash: 5733c60024f057a436a1e2fd1fdb86ee208496d2
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63373941"
---
# <a name="mapi-address-book-provider-overview"></a>Vue d’ensemble du fournisseur de carnet d’adresses MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnets d’adresses gèrent l’accès aux informations d’annuaire. Les informations d’annuaire sont constituées de données pour deux types de destinataires de message : les utilisateurs de messagerie individuels et les groupes d’utilisateurs de messagerie fréquemment adressés ensemble dans des listes de distribution. Selon le type de destinataire et le fournisseur de carnet d’adresses, un large éventail d’informations peuvent être disponibles. Par exemple, tous les fournisseurs de carnet d’adresses stockent le nom, l’adresse et le type d’adresse d’un destinataire.
  
Chaque fournisseur de carnet d’adresses organise ces données à l’aide d’un ou plusieurs conteneurs. Le nombre et la structure des conteneurs dépendent de l’implémentation du fournisseur de carnet d’adresses. Par exemple, un fournisseur de carnet d’adresses peut utiliser un seul conteneur pour contenir toutes les informations, un autre peut utiliser un conteneur de niveau supérieur qui contient des sous-conteneurs et un troisième peut utiliser plusieurs conteneurs de niveau supérieur, chacun contenant des sous-conteneurs. Une hiérarchie de conteneur de carnet d’adresses peut être assez profonde ; il n’existe aucune limite au nombre de sous-ensembles qui peuvent être utilisés.
  
L’illustration suivante illustre une organisation de carnet d’adresses MAPI classique.
  
**Organisation de carnet d’adresses**
  
![Organisation de carnet d’adresses](media/amapi_04.gif "Organisation de carnet d’adresses")
  
MAPI intègre toutes les informations fournies par les fournisseurs de carnets d’adresses installés dans un carnet d’adresses unique, en présentant un affichage unifié à l’application cliente. La liste intégrée affiche les conteneurs de niveau supérieur affichés par chacun des fournisseurs de carnet d’adresses installés. La plupart des fournisseurs de carnet d’adresses exposent uniquement quelques conteneurs (généralement un à trois) au niveau supérieur pour être inclus dans le niveau supérieur du carnet d’adresses intégré MAPI. Par exemple, un fournisseur de carnet d’adresses peut rendre disponibles « Tous les utilisateurs » et « Utilisateurs locaux » en tant que deux conteneurs au niveau supérieur.
  
Les utilisateurs d’applications clientes peuvent afficher le contenu des conteneurs de carnet d’adresses et, dans certains cas, en modifier le contenu. Les conteneurs de carnet d’adresses peuvent être créés avec différents niveaux d’accès, selon le fournisseur de carnet d’adresses. 
  
## <a name="see-also"></a>Voir aussi

- [Fonctionnalités et architecture MAPI](mapi-features-and-architecture.md)

