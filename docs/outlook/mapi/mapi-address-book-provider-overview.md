---
title: Vue d'ensemble du fournisseur de carnets d'adresses MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ee628f4b11cb174c05a16ca60c9ec830a0e9abbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426540"
---
# <a name="mapi-address-book-provider-overview"></a>Vue d'ensemble du fournisseur de carnets d'adresses MAPI
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de carnet d'adresses gèrent l'accès aux informations d'annuaire. Les informations d'annuaire sont constituées de données pour deux types de destinataires de message: les utilisateurs de messagerie individuels et les groupes d'utilisateurs de messagerie qui sont généralement regroupés dans les listes de distribution. En fonction du type de destinataire et du fournisseur de carnets d'adresses, il existe un large éventail d'informations pouvant être mises à disposition. Par exemple, tous les fournisseurs de carnets d'adresses stockent le nom, l'adresse et le type d'adresse d'un destinataire.
  
Chaque fournisseur de carnet d'adresses organise ces données à l'aide d'un ou de plusieurs conteneurs. Le nombre et la structure des conteneurs dépend de l'implémentation du fournisseur de carnet d'adresses. Par exemple, un fournisseur de carnet d'adresses peut utiliser un conteneur unique pour conserver toutes les informations, un autre peut utiliser un conteneur de niveau supérieur qui contient des sous-conteneurs, et un troisième peut utiliser plusieurs conteneurs de niveau supérieur, chacun contenant des sous-conteneurs. Une hiérarchie de conteneur de carnet d'adresses peut être assez profonde; Il n'existe pas de limite au nombre de sous-conteneurs pouvant être utilisés.
  
L'illustration suivante montre une organisation de carnet d'adresses MAPI standard.
  
**Organisation de carnet d’adresses**
  
![Organisation du carnet d'adresses] (media/amapi_04.gif "Organisation du carnet d'adresses")
  
MAPI intègre toutes les informations fournies par les fournisseurs de carnets d'adresses installés dans un seul carnet d'adresses, présentant une vue unifiée à l'application cliente. La liste intégrée affiche les conteneurs de niveau supérieur affichés par chacun des fournisseurs de carnets d'adresses installés. La plupart des fournisseurs de carnets d'adresses n'exposent qu'un petit nombre de conteneurs (généralement 1 à 3) au niveau supérieur pour l'inclusion au niveau supérieur du carnet d'adresses intégré MAPI. Par exemple, un fournisseur de carnets d'adresses peut mettre à disposition «tous les utilisateurs» et «utilisateurs locaux» en tant que deux conteneurs au niveau supérieur.
  
Les utilisateurs des applications clientes peuvent afficher le contenu des conteneurs du carnet d'adresses et, dans certains cas, modifier le contenu. Les conteneurs du carnet d'adresses peuvent être créés avec différents niveaux d'accès, en fonction du fournisseur de carnet d'adresses. 
  
## <a name="see-also"></a>Voir aussi

- [Architecture et fonctionnalités MAPI](mapi-features-and-architecture.md)

