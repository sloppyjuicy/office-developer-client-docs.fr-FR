---
title: Documentation de valeur de retour MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c32ee53c-b063-4a00-a6bf-75ce5e07f56a
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f2b8f87987f93ec152d4986131a6b7990273c28d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784695"
---
# <a name="mapi-return-value-documentation"></a>Documentation de valeur de retour MAPI

  
  
**S’applique à**: Outlook 
  
Les entrées de référence dans ce guide de référence du document uniquement les valeurs de retour qui nécessitent une gestion par les applications clientes. Valeurs de retour qui indiquent les erreurs courantes et peuvent être déduites en vérifiant les échecs ne figurent pas dans la documentation. Par exemple, de nombreuses méthodes de l’interface peuvent renvoyer MAPI_E_INVALID_PARAMETER si un appelant spécifie une valeur incorrecte pour un paramètre d’entrée. Cette valeur n’est généralement pas répertoriée dans l’ensemble de valeurs de retour attendus, car il est inutile de vérifier spécifiquement pour MAPI_E_INVALID_PARAMETER et pas nécessaire de traiter de façon différente à partir de n’importe quel autre erreur. En revanche, certains fournisseurs de services ne prennent pas en charge la notification d’événement et retourne à la méthode **Advise** effectuée par les clients par le biais de **IMAPISession**MAPI_E_NO_SUPPORT. Étant donné que les clients doivent vérifier cette valeur et fournissent le code pour traiter la condition qu’il représente doit explicitement, il se produit, MAPI_E_NO_SUPPORT est inclus dans la liste des valeurs de retour pour [IMAPISession::Advise](imapisession-advise.md).
  
Le tableau suivant décrit les valeurs d’erreur qui sont généralement renvoyés à partir de méthodes et les fonctions et requièrent une gestion explicite par un client ou fournisseur de services. Ces valeurs sont répartis en quatre catégories : valeurs qui indiquent des données d’entrée non valides, les valeurs qui indiquent des problèmes de ressources, les valeurs qui indiquent l’incompatibilité du jeu de caractères et les valeurs qui indiquent l’échec d’une origine inconnue.
  
|**Valeur renvoyée**|**Description**|
|:-----|:-----|
|MAPI_E_INVALID_PARAMETER  <br/> |Un ou plusieurs des paramètres transmis à la méthode ou fonctions ne sont pas valides.  <br/> |
|MAPI_E_UNKNOWN_FLAGS  <br/> |Une ou plusieurs valeurs pour un paramètre indicateurs ne sont pas valides.  <br/> |
|MAPI_E_DISK_ERROR  <br/> |Il y a un problème d’écriture ou de lecture à partir du disque.  <br/> |
|MAPI_E_NOT_ENOUGH_DISK  <br/> |Pas de suffisamment d’espace disque était disponible pour terminer l’opération.  <br/> |
|MAPI_E_NOT_ENOUGH_MEMORY  <br/> |Mémoire insuffisante était disponible pour terminer l’opération.  <br/> |
|MAPI_E_NOT_ENOUGH_RESOURCES  <br/> |Pas de suffisamment de ressources système était disponibles pour terminer l’opération.  <br/> |
|MAPI_E_BAD_CHARWIDTH  <br/> |Il existe une incompatibilité dans les jeux de caractères pris en charge par l’appelant et l’implémentation.  <br/> |
|MAPI_E_CALL_FAILED  <br/> |Une erreur d’origine inattendu ou inconnu s’est produite.  <br/> |
   
Les constantes qui représentent les valeurs de retour MAPI sont répertoriés dans le MAPICODE. Fichier d’en-tête H. Certaines de ces constantes mappent aux erreurs Win32 ; Vous trouverez le mappage de ces constantes pour les valeurs numériques dans le fichier d’en-tête Win32 WINERROR. H.
  
Erreurs concernant les données non valides sont passées par l’appelant peuvent être déterminés par le biais soit les paramètre validation des fonctions de l’API fournies par MAPI ou un ensemble de macros. 
  
Incompatibilité de jeu de caractères se produit lorsque une des situations suivantes se produit :
  
- Un client ou fournisseur de services définit l’indicateur MAPI_UNICODE sur un appel de méthode ou la fonction et l’implémentation ne prend pas en charge Unicode. Définition MAPI_UNICODE indique que les chaînes de caractères transmis comme entrée sont des chaînes Unicode et que des chaînes de caractères transmis en sortie doivent être des chaînes Unicode.
    
- Un client ou fournisseur de services ne définit pas l’indicateur MAPI_UNICODE sur un appel de méthode ou la fonction et l’implémentation prend uniquement en charge Unicode.
    

