---
title: Définition de nouvelles propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
ms.openlocfilehash: 063be5762b9365c98660e4f8f12fa557f320a627
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522246"
---
# <a name="defining-new-mapi-properties"></a>Définition de nouvelles propriétés MAPI

**S’applique à** : Outlook 2013 | Outlook 2016
  
En dépit de la richesse des propriétés fournies par MAPI pour une utilisation par les clients et les fournisseurs de services, MAPI permet de créer de nouvelles propriétés si nécessaire. Certains des scénarios valides pour définir de nouvelles propriétés publiques incluent un client créant des propriétés pour prendre en charge une nouvelle classe de message et un fournisseur de services créant de nouvelles propriétés pour exposer des fonctionnalités de système de messagerie uniques.
  
Il n’est généralement pas valide pour un fournisseur de services de définir de nouvelles propriétés pour un objet MAPI existant ou une classe de message. L’un des principaux avantages de l’utilisation de MAPI est que les identificateurs et formats standard d’un grand nombre d’éléments système de messagerie sont mis en place, ce qui permet aux utilisateurs de combiner et de faire correspondre les fournisseurs de services de façon transparente. Les fournisseurs de services qui utilisent des propriétés non normes ne fonctionnent pas aussi bien avec d’autres fournisseurs de services.
  
Les clients peuvent créer des propriétés de contenu pour de nouvelles classes de messages en :
  
- Utilisation d’identificateurs de propriétés dans une plage désignée pour les propriétés de contenu spécifiques à la classe de message.

  - Ou -

- Utilisation de propriétés nommées.

La première option est préférable, car tous les fournisseurs de services ne sont pas en charge les propriétés nommées. MAPI définit deux plages distinctes que les clients peuvent utiliser pour les nouvelles propriétés de contenu spécifiques à la classe de message :
  
- 0x6800 à 0x7BFF propriétés transmises

- 0x7C00 à 0x7FFF propriétés nontransmitables

Les identificateurs de propriété doivent se trouver dans des plages prédéfines pour éviter les collisions entre les propriétés définies par différents fournisseurs ou utilisateurs. Toutefois, les utilisateurs de propriétés dans ces plages ne peuvent pas faire d’hypothèses quant au comportement des propriétés. Chaque client qui crée une classe de message a accès à ces plages ; une propriété avec identificateur _xxxx_ peut signifier un comportement pour une classe de message et un autre comportement pour une autre classe de message.
  
Les propriétés nommées sont utilisées pour garantir qu’une propriété spécifique est propre à une classe de message. Les identificateurs de propriété nommés commencent dans 0x8000 plage. Les clients définissent un ou plusieurs noms, puis appellent la méthode [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) de la boutique de messages pour associer un identificateur à chaque nom. Les propriétés nommées peuvent être utilisées par les clients ou les fournisseurs de services pour définir de nouvelles propriétés pour n’importe quel objet uniquement si le propriétaire de l’objet prend en charge les propriétés nommées. Les utilisateurs de ces **propriétés appellent GetIDsFromNames** et une méthode **IMAPIProp** associée, [GetNamesFromIDs](imapiprop-getnamesfromids.md), pour faire la distinction entre un nom et son identificateur.
  
Toutes les propriétés, nouvelles ou existantes, doivent utiliser l’ensemble des types de propriétés prédéfincis. Les nouveaux types de propriétés ne peuvent pas être ajoutés et les types existants ne peuvent pas être modifiés ou supprimés. Les propriétés simples et de petite taille, telles que les propriétés d’un seul caractère ou d’un nombre d’nombres de 16 bits, peuvent être stockées dans n’importe quel type approprié. Par exemple, les integers peuvent être stockés en **tant qu’ULONG** et les chaînes peuvent être stockées sous forme **PT_STRING8**.
  
Utilisez le **PT_BINARY** type pour indiquer un tableau d’byte compté. Ce type de propriété est utile pour étendre les types de données qui peuvent être stockés dans un objet. Les octets sont transmis dans l’ordre et aucune hypothèse n’est faite sur la signification des données. Lorsqu’une application cliente lit des données d’une telle propriété, les données restent inchangées par rapport à leur façon de les stocker. Le client doit effectuer le permutation d’byte nécessaire lors du déplacement des données entre les processeurs.
  
## <a name="see-also"></a>Voir aussi

[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)
