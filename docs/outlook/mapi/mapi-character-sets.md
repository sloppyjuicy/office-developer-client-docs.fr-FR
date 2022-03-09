---
title: Jeux de caractères MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
ms.openlocfilehash: 4b4d524036f44439540ee768b589392e43a4523c
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63372856"
---
# <a name="mapi-character-sets"></a>Jeux de caractères MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les applications clientes et les fournisseurs de services compatibles MAPI peuvent utiliser des caractères ANSI (un seul sur deux caractères) ou unicode (sur deux caractères). Les jeux de caractères OEM ne sont pas pris en charge. Une chaîne OEM transmise à une méthode ou une fonction MAPI entraîne l’échec de cette méthode ou fonction. Les applications clientes qui fonctionnent avec des noms de fichiers dans le jeu de caractères OEM doivent être attentives à les convertir en ANSI avant de les transmettre à une méthode ou une fonction MAPI.
  
La prise en charge du jeu de caractères Unicode est facultative, à la fois pour les clients et les fournisseurs de services. Tous les fournisseurs de services doivent écrire leur code afin qu’ils soient compilés, qu’ils soient ou non en charge Unicode. Les clients sont compilés de manière conditionnable, en fonction de leur niveau de support, mais pas les fournisseurs de services. Elles ne doivent pas être recompilées lorsque le jeu de caractères change. Rien dans le code du fournisseur de services ne doit être conditionnel. 
  
Lorsque des clients ou des fournisseurs de services qui supportent Unicode appellent une méthode qui inclut des chaînes de caractères comme paramètres d’entrée ou de sortie, ils définissent l’MAPI_UNICODE de sortie. La définition de cet indicateur indique à l’implémentation que toutes les chaînes entrantes sont des chaînes Unicode. Lors de la sortie, la définition de cet indicateur demande que toutes les chaînes passées à partir de l’implémentation soient des chaînes Unicode si possible. Les implémenteurs de méthodes qui la prise en charge d’Unicode seront conformes à la demande ; les implémenteurs de méthode qui ne fournissent pas de prise en charge Unicode ne seront pas conformes. Les propriétés de chaîne qui ne sont pas au format Unicode sont de type PT_STRING8.
  
MAPI définit la constante **fMapiUnicode** dans le fichier d’en-tête MAPIDEFS. H pour représenter le jeu de caractères par défaut. Si un client ou un fournisseur de services prend en charge Unicode, **fMapiUnicode** est MAPI_UNICODE. Clients et fournisseurs de services qui ne prisent pas en charge Unicode **définissent fMapiUnicode** sur zéro. 
  
Les fournisseurs de services qui ne prisent pas en charge Unicode doivent :
  
- Refuser d’effectuer des conversions entre les jeux de caractères.
    
- Ne passez jamais l’indicateur MAPI_UNICODE dans les appels de méthode.
    
- Renvoyer MAPI_E_BAD_CHARWIDTH lorsque l’MAPI_UNICODE est passé.
    
- Déclarez explicitement les propriétés de chaîne ANSI. 
    
Les fournisseurs de services peuvent également renvoyer MAPI_E_BAD_CHARWIDTH lorsqu’ils ne peuvent prendre en charge Unicode et que les clients ne passent pas l’indicateur MAPI_UNICODE de service. 
  
 La version actuelle de MAPI prend en charge Unicode dans les méthodes suivantes : 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp::GetLastError](imapiprop-getlasterror.md) (**implémentation IAddrBook** uniquement) 
  
Pour ces méthodes, les appelants peuvent s’attendre à ce que les chaînes renvoyées soient des chaînes Unicode. Les chaînes de caractères renvoyées à partir des implémentations MAPI de toute autre méthode seront des chaînes de caractères ANSI.
  

