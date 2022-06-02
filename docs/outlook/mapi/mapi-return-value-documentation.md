---
title: Documentation sur la valeur de retour MAPI
description: Documente uniquement les valeurs de retour MAPI qui nécessitent une gestion par les applications clientes. Décrit les valeurs d’erreur qui sont généralement retournées à partir de méthodes et de fonctions.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
ms.openlocfilehash: 94512fb18ed726bb1d653405a8ac7d5d7da467a0
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828261"
---
# <a name="mapi-return-value-documentation"></a>Documentation sur la valeur de retour MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les entrées de référence de ce document de référence ne sont que celles qui nécessitent une certaine gestion par les applications clientes. Les valeurs de retour qui indiquent des conditions d’erreur courantes et qui peuvent être déduites en vérifiant l’échec ne sont pas incluses dans la documentation. Par exemple, de nombreuses méthodes d’interface peuvent retourner MAPI_E_INVALID_PARAMETER si un appelant spécifie la valeur incorrecte pour un paramètre d’entrée. Cette valeur n’est généralement pas répertoriée dans l’ensemble des valeurs de retour attendues, car il n’est pas nécessaire de rechercher spécifiquement MAPI_E_INVALID_PARAMETER et il n’est pas nécessaire de la traiter différemment d’une autre erreur. En revanche, certains fournisseurs de services ne prennent pas en charge la notification d’événement et retournent MAPI_E_NO_SUPPORT à la méthode **Advise** effectuée par les clients via **IMAPISession**. Étant donné que les clients doivent vérifier explicitement cette valeur et fournir du code pour gérer la condition qu’elle représente si elle se produit, MAPI_E_NO_SUPPORT est inclus dans la liste des valeurs de retour pour [IMAPISession::Advise](imapisession-advise.md).
  
Le tableau suivant décrit les valeurs d’erreur qui sont généralement retournées à partir de méthodes et de fonctions et qui nécessitent une gestion explicite de la part d’un client ou d’un fournisseur de services. Ces valeurs se répartissent en quatre catégories : les valeurs qui indiquent des données d’entrée non valides, les valeurs qui indiquent des problèmes de ressource, les valeurs qui indiquent l’incompatibilité du jeu de caractères et les valeurs qui indiquent l’échec d’une origine inconnue.
  
|**Valeur renvoyée**|**Description**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Un ou plusieurs des paramètres passés dans la méthode ou les fonctions n’étaient pas valides. |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Une ou plusieurs valeurs pour un paramètre d’indicateurs n’étaient pas valides. |
|MAPI_E_DISK_ERROR  <br/> |Il y a eu un problème d’écriture ou de lecture à partir du disque. |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |L’espace disque disponible était insuffisant pour terminer l’opération. |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |Mémoire insuffisante disponible pour terminer l’opération. |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |Les ressources système disponibles étaient insuffisantes pour terminer l’opération. |
|MAPI_E_BAD_CHARWIDTH  <br/> |Il existe une incompatibilité dans les jeux de caractères pris en charge par l’appelant et l’implémentation. |
|MAPI_E_CALL_FAILED  <br/> |Une erreur d’origine inattendue ou inconnue s’est produite. |
   
Les constantes qui représentent les valeurs de retour MAPI sont répertoriées dans MAPICODE. Fichier d’en-tête H. Certaines des constantes mappent aux erreurs Win32 ; Le mappage de ces constantes à des valeurs numériques se trouve dans le fichier d’en-tête Win32, WINERROR.H.
  
Les erreurs concernant les données non valides transmises par un appelant peuvent être déterminées via les fonctions d’API de validation de paramètre fournies par MAPI ou un ensemble de macros. 
  
Une incompatibilité de jeu de caractères se produit lorsque l’une des situations suivantes se produit :
  
- Un client ou un fournisseur de services définit l’indicateur MAPI_UNICODE sur un appel de méthode ou de fonction, et l’implémentation ne prend pas en charge Unicode. Le paramètre MAPI_UNICODE indique que les chaînes de caractères passées en entrée sont des chaînes Unicode et que les chaînes de caractères passées en tant que sortie sont censées être des chaînes Unicode.
    
- Un client ou un fournisseur de services ne définit pas l’indicateur de MAPI_UNICODE sur un appel de méthode ou de fonction et l’implémentation prend uniquement en charge Unicode.
    

