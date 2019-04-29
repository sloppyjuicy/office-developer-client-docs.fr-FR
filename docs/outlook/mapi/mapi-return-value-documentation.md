---
title: Documentation sur la valeur de retour MAPI
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
# <a name="mapi-return-value-documentation"></a>Documentation sur la valeur de retour MAPI

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Les entrées de référence de cette référence documentent uniquement les valeurs de retour qui nécessitent une gestion par les applications clientes. Les valeurs renvoyées qui indiquent des conditions d'erreur communes et peuvent être déduites en vérifiant l'échec ne sont pas incluses dans la documentation. Par exemple, de nombreuses méthodes d'interface peuvent renvoyer MAPI_E_INVALID_PARAMETER si un appelant spécifie une valeur incorrecte pour un paramètre d'entrée. Cette valeur n'est généralement pas indiquée dans le jeu de valeurs de retour attendues, car il n'est pas nécessaire de Rechercher spécifiquement MAPI_E_INVALID_PARAMETER et de ne pas le traiter différemment d'une autre erreur. En revanche, certains fournisseurs de services ne prennent pas en charge la notification d'événement et renvoient **** MAPI_E_NO_SUPPORT à la méthode Advise effectuée par les clients via **IMAPISession**. Étant donné que les clients doivent vérifier explicitement cette valeur et fournir du code pour gérer la condition qu'elle représente si elle se produit, MAPI_E_NO_SUPPORT est inclus dans la liste des valeurs de retour pour [IMAPISession:: Advise](imapisession-advise.md).
  
Le tableau suivant décrit les valeurs d'erreur qui sont couramment renvoyées à partir de méthodes et de fonctions et qui nécessitent un traitement explicite sur la partie d'un client ou d'un fournisseur de services. Ces valeurs sont divisées en quatre catégories: les valeurs qui indiquent des données d'entrée non valides, les valeurs qui indiquent des problèmes de ressource, les valeurs qui indiquent une incompatibilité de jeu de caractères et les valeurs qui indiquent l'échec d'une origine inconnue.
  
|**Valeur renvoyée**|**Description**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Un ou plusieurs des paramètres transmis à la méthode ou aux fonctions ne sont pas valides.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Une ou plusieurs valeurs pour un paramètre flags ne sont pas valides.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Un problème est survenu lors de l'écriture ou de la lecture sur le disque.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |Vous n'avez pas suffisamment d'espace disque disponible pour terminer l'opération.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |La mémoire disponible est insuffisante pour terminer l'opération.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |Les ressources système disponibles sont insuffisantes pour terminer l'opération.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |Il existe une incompatibilité dans les jeux de caractères pris en charge par l'appelant et l'implémentation.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Une erreur d'origine inattendue ou inconnue s'est produite.  <br/> |
   
Les constantes qui représentent les valeurs de retour MAPI sont répertoriées dans le MAPICODE. Fichier d'en-tête H. Certaines des constantes sont mappées à des erreurs Win32; le mappage de ces constantes aux valeurs numériques se trouve dans le fichier d'en-tête Win32 WINERROR. H.
  
Les erreurs relatives aux données non valides transmises par un appelant peuvent être déterminées via les fonctions de l'API de validation de paramètres fournies par MAPI ou un ensemble de macros. 
  
L'incompatibilité des jeux de caractères survient lorsque l'une des situations suivantes se produit:
  
- Un client ou un fournisseur de services définit l'indicateur MAPI_UNICODE sur un appel de méthode ou de fonction et l'implémentation ne prend pas en charge Unicode. Le paramètre MAPI_UNICODE indique que les chaînes de caractères transmises comme entrée sont des chaînes Unicode et que les chaînes de caractères renvoyées en tant que sortie sont supposées être des chaînes Unicode.
    
- Un fournisseur de services ou de clients ne définit pas l'indicateur MAPI_UNICODE sur un appel de méthode ou de fonction et l'implémentation prend uniquement en charge Unicode.
    

