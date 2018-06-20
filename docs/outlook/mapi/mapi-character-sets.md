---
title: Jeux de caractères MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 3f94823eb3f90ff9ac0f472a2de64e1904920d9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784583"
---
# <a name="mapi-character-sets"></a>Jeux de caractères MAPI

  
  
**S’applique à**: Outlook 
  
Applications clientes compatibles MAPI et les fournisseurs de services peuvent utiliser des caractères ANSI (octet) ou Unicode (deux octets). Jeux de caractères OEM ne sont pas pris en charge. Une chaîne OEM transmis à une méthode MAPI ou la fonction entraînera cette méthode ou la fonction en échec. Les applications clientes qui fonctionnent avec les noms de fichiers dans le jeu de caractères OEM doivent être prudent pour les convertir au format ANSI avant de les passer à une méthode MAPI ou une fonction.
  
Prise en charge Unicode jeu de caractères est facultatif, à la fois pour les clients et les fournisseurs de services. Tous les fournisseurs de services doivent écrire leur code afin qu’ils pour pouvoir compiler indépendamment ou non qu’ils prennent en charge Unicode. Clients de compilation conditionnelle, en fonction de leur niveau de prise en charge, mais n’est pas le cas des fournisseurs de services. Ils devront pas être recompilées lors de la modification du jeu de caractères. Nothing dans le code de fournisseur de service doit être conditionnelle. 
  
Lorsque les clients ou fournisseurs de services qui prennent en charge Unicode émettre un appel de méthode qui inclut des chaînes de caractères en tant que paramètres d’entrée ou de sortie, ils définir l’indicateur MAPI_UNICODE. Définition de cet indicateur indique à l’implémentation que toutes les chaînes entrants sont des chaînes Unicode. Dans la sortie, définition de cet indicateur demandes que toutes les chaînes passées à partir de l’implémentation doit être chaînes Unicode si possible. L’implémentation de méthode qui prennent en charge Unicode est conformes à la demande ; l’implémentation de méthode qui ne fournit pas de prise en charge Unicode n’est pas conforme. Propriétés de type chaîne qui ne sont pas au format Unicode sont de type PT_STRING8.
  
MAPI définit la constante **fMapiUnicode** dans le fichier d’en-tête MAPIDEFS. H pour représenter le jeu de caractères par défaut. Si un client ou fournisseur de services prend en charge Unicode, **fMapiUnicode** est définie sur MAPI_UNICODE. Clients et fournisseurs de services qui ne prennent pas en charge Unicode **fMapiUnicode** la valeur zéro. 
  
Fournisseurs de services qui ne prennent pas en charge Unicode doivent :
  
- Refuser effectuer des conversions entre les jeux de caractères.
    
- L’indicateur MAPI_UNICODE jamais passer des appels de méthode.
    
- Retourner MAPI_E_BAD_CHARWIDTH lors de l’indicateur MAPI_UNICODE est passé.
    
- Déclarer explicitement les propriétés de type chaîne ANSI. 
    
Fournisseurs de services peuvent également retourner MAPI_E_BAD_CHARWIDTH lorsqu’elles prennent uniquement en charge Unicode et les clients ne passent pas l’indicateur MAPI_UNICODE. 
  
 La version actuelle de MAPI prend en charge Unicode dans les méthodes suivantes : 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (Implémentation**IAddrBook** uniquement) 
  
Pour ces méthodes, les appelants peuvent s’attendre toutes les chaînes renvoyées à des chaînes Unicode. Chaînes de caractères renvoyées à partir des implémentations MAPI de toute autre méthode seront des chaînes de caractères ANSI.
  

