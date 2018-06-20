---
title: Codes d’erreur de fournisseur Outlook Social Connector
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0799243e-ba92-44c4-b687-182e50b57cb7
description: Fournisseurs doivent renvoyer des erreurs à l’appelant à l’aide d’un des codes d’erreur affichés dans le tableau suivant.
ms.openlocfilehash: 9e9abfda5930926a873ac37d3372eff7100be8a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787703"
---
# <a name="outlook-social-connector-provider-error-codes"></a>Codes d’erreur de fournisseur Outlook Social Connector

Fournisseurs doivent renvoyer des erreurs à l’appelant à l’aide d’un des codes d’erreur affichés dans le tableau suivant. 
  
|**Erreur**|**Code d’erreur (hexadécimal)**|**Description**|
|:-----|:-----|:-----|
|OSC_E_AUTH_ERROR  <br/> |0x80041404  <br/> |Échec de l’authentification sur le réseau du site de réseau social.  <br/> |
|OSC_E_COULDNOTCONNECT  <br/> |0x80041402  <br/> |Aucune connexion n’est disponible pour se connecter au site de réseau social.  <br/> |
|OSC_E_FAIL  <br/> |0 x 80004005  <br/> |Erreur de défaillance générale.  <br/> |
|OSC_E_INTERNAL_ERROR  <br/> |0x80041400  <br/> |Une erreur interne s’est produite en raison d’une opération non valide.  <br/> |
|OSC_E_INVALIDARG (E_INVALIDARG)  <br/> |0 x 80070057  <br/> |Un argument non valide a été passé à une fonction.  <br/> |
|OSC_E_NO_CHANGES  <br/> |0x80041406  <br/> |Aucune modification n’ont eu lieu depuis la dernière synchronisation.  <br/> |
|OSC_E_NOT_FOUND  <br/> |0x80041405  <br/> |Impossible de trouver une ressource.  <br/> |
|OSC_E_NOT_IMPLEMENTED (E_NOTIMPL)  <br/> |0x80004001  <br/> |La demande pour le site de réseau social est valide mais n’a pas été implémentée par le site de réseau social.  <br/> |
|OSC_E_OUT_OF_MEMORY (E_OUTOFMEMORY)  <br/> |0x8007000E  <br/> |Une erreur de mémoire insuffisante s’est produite.  <br/> |
|OSC_E_PERMISSION_DENIED  <br/> |0x80041403  <br/> |Le fournisseur OSC autorisés pour la ressource.  <br/> |
|OSC_E_SERVER_VERSION_NOT_SUPPORTED  <br/> |0x80041406  <br/> |La version du serveur à configurer le compte de réseau social n’est pas pris en charge.  <br/> |
|OSC_E_VERSION  <br/> |0x80041401  <br/> |Le fournisseur ne prend pas en charge cette version de l’extensibilité de fournisseur OSC.  <br/> |
   
## <a name="remarks"></a>Remarques

Réussite, avertissement et valeurs d’erreur sont renvoyés à l’aide d’un nombre à 32 bits qui est appelé une poignée de résultat, **HRESULT**. Un **HRESULT** n’est pas un handle vers rien ; Il est simplement une valeur 32 bits qui comporte plusieurs champs codés dans la valeur. Un résultat positif indique une réussite avec état, un résultat de zéro indique la réussite sans statut (S_OK) et un résultat négatif indique l’échec. 
  

