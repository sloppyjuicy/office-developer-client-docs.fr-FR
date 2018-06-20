---
title: Vue d’ensemble du fournisseur MAPI adresse téléchargeable
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ead51434-ae19-4c34-aa7a-bdeeccca5bd9
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 4bd64aadd5fc18ba79a8717a5c58df72cd3695ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784553"
---
# <a name="mapi-address-book-provider-overview"></a>Vue d’ensemble du fournisseur MAPI adresse téléchargeable
  
**S’applique à**: Outlook 
  
Carnet d’adresses fournisseurs poignée de l’accès aux informations d’annuaire. Informations d’annuaire se composent de données pour deux types de destinataires du message : individuels de messagerie des utilisateurs et groupes d’utilisateurs de messagerie qui sont généralement traités ensemble dans des listes de distribution. Selon le type de destinataire et le fournisseur de carnet d’adresses, il est un large éventail d’informations qui peuvent être rendues disponibles. Par exemple, tous les fournisseurs de carnet d’adresses stockent le nom, adresse et type d’adresse d’un destinataire.
  
Chaque fournisseur de carnet d’adresses organise ces données à l’aide d’un ou plusieurs conteneurs. Le nombre et la structure des conteneurs varie selon l’implémentation du fournisseur de carnet d’adresses. Par exemple, un fournisseur de carnet d’adresses peut utiliser un seul conteneur pour stocker toutes les informations, une autre peut utiliser un conteneur de niveau supérieur qui contient les sous-conteneurs et une troisième peut utiliser plusieurs conteneurs de niveau supérieur, chaque sous-conteneurs de cette dernière. Une hiérarchie de conteneur de carnets d’adresses peut être très profonde ; Il n’existe aucune limite au nombre de sous-conteneurs qui peut être utilisé.
  
L’illustration suivante montre une organisation de carnet d’adresses MAPI par défaut.
  
**Organisation de carnet d’adresses**
  
![Organisation de carnet d’adresses] (media/amapi_04.gif "Organisation de carnet d’adresses")
  
MAPI intègre toutes les informations fournies par les fournisseurs de carnet d’adresses installé dans un carnet d’adresses unique, présentant une vue unifiée à l’application cliente. La liste intégrée affiche les conteneurs de niveau supérieur affichés par chacun des fournisseurs de carnet d’adresses installé. La plupart des fournisseurs de carnet d’adresses exposent uniquement quelques conteneurs (généralement une 1 à 3) au niveau supérieur à inclure dans la partie supérieure du carnet d’adresses intégré MAPI. Par exemple, un fournisseur de carnet d’adresses peut rendre disponibles « tous les utilisateurs » et « Local » en tant que deux conteneurs de premier niveau.
  
Les utilisateurs d’applications clientes peuvent afficher le contenu de conteneurs de carnet d’adresses et, dans certains cas, modifier le contenu. Conteneurs de carnet d’adresses peuvent être créés avec différents niveaux d’accès, selon le fournisseur de carnet d’adresses. 
  
## <a name="see-also"></a>Voir aussi

- [Architecture et des fonctionnalités MAPI](mapi-features-and-architecture.md)

