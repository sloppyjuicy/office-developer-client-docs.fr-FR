---
title: Documentation sur les valeurs de retour MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 5bbafe9fda479d951bb20175ab904dc6e241226a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429690"
---
# <a name="mapi-return-value-documentation"></a>Documentation sur les valeurs de retour MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les entrées de référence dans ce document de référence ne retournent que les valeurs de retour qui nécessitent une certaine gestion par les applications clientes. Les valeurs de retour qui indiquent des conditions d’erreur courantes et qui peuvent être déduites en vérifiant l’échec ne sont pas incluses dans la documentation. Par exemple, de nombreuses méthodes d’interface peuvent renvoyer MAPI_E_INVALID_PARAMETER si un appelant spécifie une valeur erronée pour un paramètre d’entrée. Cette valeur n’est généralement pas répertoriée dans l’ensemble des valeurs de retour attendues, car il n’est pas nécessaire de rechercher des MAPI_E_INVALID_PARAMETER spécifiquement et de la traiter différemment d’une autre erreur. En revanche, certains fournisseurs de services ne peuvent pas prendre en charge la notification d’événement et retournent des MAPI_E_NO_SUPPORT à la méthode **Advise** réalisée par les clients via **IMAPISession**. Étant donné que les clients doivent vérifier explicitement cette valeur et fournir du code pour gérer la condition qu’elle représente si elle se produit, MAPI_E_NO_SUPPORT est inclus dans la liste des valeurs de retour pour [IMAPISession::Advise](imapisession-advise.md).
  
Le tableau suivant décrit les valeurs d’erreur qui sont généralement renvoyées à partir de méthodes et de fonctions et nécessitent une gestion explicite de la part d’un client ou d’un fournisseur de services. Ces valeurs sont dans quatre catégories : les valeurs qui indiquent des données d’entrée non valides, les valeurs qui indiquent des problèmes de ressources, les valeurs qui indiquent l’incompatibilité de jeu de caractères et les valeurs qui indiquent l’échec d’une origine inconnue.
  
|**Valeur renvoyée**|**Description**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Un ou plusieurs des paramètres passés dans la méthode ou les fonctions n’étaient pas valides.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Une ou plusieurs valeurs pour un paramètre d’indicateurs n’étaient pas valides.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Un problème est à l’écriture ou à la lecture sur le disque.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |L’espace disque disponible était insuffisant pour terminer l’opération.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |La mémoire disponible n’était pas suffisante pour terminer l’opération.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |Il n’y avait pas assez de ressources système disponibles pour terminer l’opération.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |Il existe une incompatibilité dans les jeux de caractères pris en charge par l’appelant et l’implémentation.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Une erreur d’origine inattendue ou inconnue s’est produite.  <br/> |
   
Les constantes qui représentent les valeurs de retour MAPI sont répertoriées dans MAPICODE. Fichier d’en-tête H. Certaines de ces constantes sont m mondes aux erreurs Win32 ; Le mappage de ces constantes aux valeurs numériques se trouve dans le fichier d’en-tête Win32, WINERROR.H.
  
Les erreurs concernant les données non valides transmises par un appelant peuvent être déterminées par le biais des fonctions d’API de validation des paramètres fournies par MAPI ou d’un ensemble de macros. 
  
L’incompatibilité de jeu de caractères survient lorsque l’une des situations suivantes se produit :
  
- Un client ou un fournisseur de services définit l’indicateur MAPI_UNICODE sur un appel de méthode ou de fonction et l’implémentation ne prend pas en charge Unicode. La MAPI_UNICODE indique que les chaînes de caractères transmises en tant qu’entrées sont des chaînes Unicode et que les chaînes de caractères transmises en tant que sortie sont des chaînes Unicode.
    
- Un client ou un fournisseur de services ne définisse pas l’indicateur MAPI_UNICODE sur un appel de méthode ou de fonction et l’implémentation prend uniquement en charge Unicode.
    

