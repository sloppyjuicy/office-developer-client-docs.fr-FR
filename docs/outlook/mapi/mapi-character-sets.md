---
title: Jeux de caractères MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe63916-b3eb-4ea7-bc42-80a8b0281b03
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 898883d8c93b69762883a502b7a4313b3417d0d3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417552"
---
# <a name="mapi-character-sets"></a>Jeux de caractères MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les fournisseurs de services et les applications clientes conformes à la norme MAPI peuvent utiliser des caractères ANSI (codés sur un octet) ou Unicode (double octet). Les jeux de caractères OEM ne sont pas pris en charge. Une chaîne OEM transmise à une méthode ou à une fonction MAPI entraîne l'échec de cette méthode ou fonction. Les applications clientes qui fonctionnent avec des noms de fichier dans le jeu de caractères OEM doivent être converties en ANSI avant de les transmettre à une méthode ou à une fonction MAPI.
  
La prise en charge du jeu de caractères Unicode est facultative pour les clients et les fournisseurs de services. Tous les fournisseurs de services doivent écrire leur code afin qu'ils puissent effectuer une compilation, qu'ils prennent ou non en charge Unicode. Les clients sont compilés de manière conditionnelle, en fonction de leur niveau de prise en charge, mais pas des fournisseurs de services. Elles ne doivent pas être recompilées lorsque le jeu de caractères est modifié. Nothing dans le code du fournisseur de services doit être conditionnel. 
  
Lorsque des clients ou des fournisseurs de services qui prennent en charge Unicode effectuent un appel de méthode qui inclut des chaînes de caractères comme paramètres d'entrée ou de sortie, ils définissent l'indicateur MAPI_UNICODE. La définition de cet indicateur indique à l'implémentation que toutes les chaînes entrantes sont des chaînes Unicode. Lors de la sortie, la définition de cet indicateur demande que toutes les chaînes transmises à partir de l'implémentation soient des chaînes Unicode dans la mesure du possible. Les implémenteurs de méthode qui prennent en charge Unicode seront conformes à la demande; les implémenteurs de méthodes qui ne fournissent pas de prise en charge d'Unicode ne seront pas conformes. Les propriétés de chaîne qui ne sont pas au format Unicode sont de type PT_STRING8.
  
MAPI définit la constante **fMapiUnicode** dans le fichier d'en-tête MAPIDEFS. H pour représenter le jeu de caractères par défaut. Si un client ou un fournisseur de services prend en charge Unicode, **fMapiUnicode** est défini sur MAPI_UNICODE. Les clients et fournisseurs de services qui ne prennent pas en charge Unicode Set **fMapiUnicode** sur zéro. 
  
Les fournisseurs de services qui ne prennent pas en charge Unicode doivent:
  
- Refuser d'effectuer des conversions entre des jeux de caractères.
    
- Ne transmettez jamais l'indicateur MAPI_UNICODE dans les appels de méthode.
    
- Renvoie MAPI_E_BAD_CHARWIDTH lorsque l'indicateur MAPI_UNICODE est passé.
    
- Déclarez explicitement les propriétés de chaîne ANSI. 
    
Les fournisseurs de services peuvent également renvoyer MAPI_E_BAD_CHARWIDTH lorsqu'ils prennent en charge uniquement Unicode et que les clients ne passent pas l'indicateur MAPI_UNICODE. 
  
 La version actuelle de MAPI prend en charge Unicode dans les méthodes suivantes: 
  
[IAddrBook::Address](iaddrbook-address.md)
  
[IAddrBook::CreateOneOff](iaddrbook-createoneoff.md)
  
[IAddrBook::Details](iaddrbook-details.md)
  
[IAddrBook::ResolveName](iaddrbook-resolvename.md)
  
[IMAPIProp:: GetLastError](imapiprop-getlasterror.md) (Implémentation**IAddrBook** uniquement) 
  
Pour ces méthodes, les appelants peuvent s'attendre à ce que toutes les chaînes renvoyées soient des chaînes Unicode. Les chaînes de caractères renvoyées par les implémentations MAPI de n'importe quelle autre méthode sont des chaînes de caractères ANSI.
  

