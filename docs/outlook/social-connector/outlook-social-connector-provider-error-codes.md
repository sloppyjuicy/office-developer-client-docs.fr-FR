---
title: Outlook codes d’erreur du fournisseur Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: Les fournisseurs doivent renvoyer des erreurs à l’appelant à l’aide de l’un des codes d’erreur indiqués dans le tableau suivant.
ms.openlocfilehash: e3bcbeffc054138ba866f99549b2991c30ed3d15
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787596"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Outlook codes d’erreur du fournisseur Social Connector

Les fournisseurs doivent renvoyer des erreurs à l’appelant à l’aide de l’un des codes d’erreur indiqués dans le tableau suivant. 
  
|**Erreur**|**Code d’erreur (hexadécimal)**|**Description**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |Échec de l’authentification sur le réseau du site de réseau social. |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |Aucune connexion n’est disponible pour se connecter au site de réseau social. |
|OSC_E_FAIL  <br/> |0x80004005  <br/> |Erreur d’échec générale. |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |Une erreur interne s’est produite en raison d’une opération non valide. |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0x80070057  <br/> |Un argument non valide a été transmis à une fonction. |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |Aucune modification n’a été apportée depuis la dernière synchronisation. |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |Impossible de trouver une ressource. |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |La demande au site de réseau social est valide mais n’a pas été implémentée par le site de réseau social. |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |Une erreur de mémoire est survenue. |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |Le fournisseur OSC a refusé l’autorisation pour la ressource. |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |La version du serveur pour configurer le compte de réseau social n’est pas prise en charge. |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |Le fournisseur ne prend pas en charge cette version de l’extensibilité du fournisseur OSC. |
   
## <a name="remarks"></a>Remarques

Les valeurs de réussite, d’avertissement et d’erreur sont renvoyées à l’aide d’un nombre 32 bits appelé handle de résultats, **ou HRESULT**. Un **HRESULT n’est** pas un handle vers quoi que ce soit ; Il s’agit simplement d’une valeur 32 bits dont plusieurs champs sont codés dans la valeur. Un résultat positif indique une réussite avec un état, un zéro indique une réussite sans état (S_OK) et un résultat négatif indique un échec. 
  

