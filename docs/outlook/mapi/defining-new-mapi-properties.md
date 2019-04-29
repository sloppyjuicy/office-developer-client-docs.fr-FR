---
title: Définition de nouvelles propriétés MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1a2325ea-ddfa-480f-b65f-f5b20471fb40
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 666ee413319765e39e25d586208f764afc93ae6b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425014"
---
# <a name="defining-new-mapi-properties"></a>Définition de nouvelles propriétés MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Malgré le grand éventail de propriétés fournies par MAPI pour les clients et les fournisseurs de services, MAPI permet de créer de nouvelles propriétés si nécessaire. Certains des scénarios valides pour la définition de nouvelles propriétés publiques incluent un client qui crée des propriétés pour prendre en charge une nouvelle classe de message et un fournisseur de services qui crée de nouvelles propriétés pour exposer des fonctionnalités de système de messagerie uniques.
  
En règle générale, il n'est pas valide pour un fournisseur de services de définir de nouvelles propriétés pour un objet MAPI ou une classe de message existant. L'un des principaux avantages de l'utilisation de MAPI est que les identificateurs et formats standard d'un grand nombre d'éléments du système de messagerie sont configurés, ce qui permet aux utilisateurs de combiner et de faire correspondre les fournisseurs de services de manière transparente. Les fournisseurs de services qui utilisent des propriétés non standard ne fonctionnent pas aussi bien avec d'autres fournisseurs de services. 
  
Les clients peuvent créer des propriétés de contenu pour les nouvelles classes de messages en procédant comme suit:
  
- Utilisation des identificateurs de propriété dans une plage désignée pour les propriétés de contenu propres à la classe de message.
    
    - Des
    
- Utilisation des propriétés nommées. 
    
La première option est préférable, car tous les fournisseurs de services ne prennent pas en charge les propriétés nommées. MAPI définit deux plages distinctes pour les clients à utiliser pour les nouvelles propriétés de contenu propres à la classe de message:
  
- 0x6800 vers 0x7BFF pour les propriétés transmissibles
    
- 0x7C00 vers 0x7FFF pour les propriétés qui ne sont pas transmissibles
    
Les identificateurs de propriété doivent faire partie de plages prédéfinies pour empêcher les collisions entre les propriétés définies par des fournisseurs ou des utilisateurs différents. Toutefois, les utilisateurs des propriétés de ces plages ne peuvent pas faire des suppositions quant au comportement des propriétés. Tous les clients qui créent une nouvelle classe de message ont accès à ces plages; une propriété avec identificateur _xxxx_ peut signifier un comportement pour une classe de message et un autre comportement pour une autre classe de message. 
  
Les propriétés nommées sont utilisées pour garantir qu'une propriété spécifique est unique à une classe de message. Les identificateurs de propriétés nommés commencent dans la plage 0x8000. Les clients définissent un ou plusieurs noms, puis appellent la méthode [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) de la Banque de messages pour associer un identificateur à chaque nom. Les propriétés nommées peuvent être utilisées par les clients ou les fournisseurs de services pour définir de nouvelles propriétés pour n'importe quel objet uniquement si le propriétaire de l'objet prend en charge les propriétés nommées. Les utilisateurs de ces propriétés appellent **GetIDsFromNames** et une méthode **IMAPIProp** associée, [GetNamesFromIDs](imapiprop-getnamesfromids.md), pour établir une correspondance entre un nom et son identificateur.
  
Toutes les propriétés, nouvelles ou existantes, doivent utiliser l'ensemble de types de propriétés prédéfinis. Les nouveaux types de propriétés ne peuvent pas être ajoutés et les types existants ne peuvent pas être modifiés ou supprimés. Les propriétés simples, de petite taille, telles que les propriétés d'entier à un seul caractère ou 16 bits, peuvent être stockées dans n'importe quel type approprié. Par exemple, des nombres entiers peuvent être stockés sous la forme **ULong** et des chaînes peuvent être stockées en tant que **PT_STRING8**. 
  
Utilisez le type **PT_BINARY** pour indiquer un tableau d'octets compté. Ce type de propriété est utile pour étendre les types de données pouvant être stockées dans un objet. Les octets sont transmis dans l'ordre et aucune hypothèse n'est faite sur la signification des données. Lorsqu'une application cliente lit des données à partir d'une telle propriété, les données ne sont pas modifiées par rapport à la façon dont elles ont été stockées. Le client doit effectuer les permutations d'octets nécessaires lors du transfert des données entre les UC. 
  
## <a name="see-also"></a>Voir aussi



[Vue d’ensemble de la propriété MAPI](mapi-property-overview.md)

