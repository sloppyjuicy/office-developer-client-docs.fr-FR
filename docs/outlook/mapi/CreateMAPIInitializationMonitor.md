---
title: CreateMAPIInitializationMonitor
manager: lindalu
ms.date: 04/26/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: 32a9758a-395d-4526-9610-3e4eeaf78c96
description: Moniteur d'initialisation MAPI
Last modified: April 26, 2021
ms.openlocfilehash: da7c48a6b026ccd4cbe4cbac192a1a0760202835
ms.sourcegitcommit: 289cececd9fa38a3f4b8a0d7fd1f86adb6be9689
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/27/2021
ms.locfileid: "52062052"
---
# <a name="createmapiinitializationmonitor"></a>CreateMAPIInitializationMonitor

**S'applique** à : Outlook 2016 | Outlook 2019
  
## <a name="mapi-initialization-monitor"></a>Moniteur d'initialisation MAPI

Parfois, une application qui utilise MAPI peut vouloir savoir quand l'initialisation est terminée. Par exemple, il a plusieurs threads qui pourraient initialiser MAPI, ou en réponse à l'initialisation de MAPI l'application souhaiterait effectuer un travail, mais ne souhaite pas toujours faire tourner la pile MAPI. Le moniteur d'initialisation fournit cette fonctionnalité via une fonction (exportée à partir de OLMAPI32.DLL) et quelques interfaces simples décrites ci-dessous.

Il s'agit du point d'entrée exporté à partir de OLMAPI32.DLL cela permet à l'appelant de récupérer une interface pour interroger l'état d'initialisation actuel, configurer un rappel pour l'achèvement de l'initialisation ou bloquer le thread actuel jusqu'à ce qu'il soit terminé. L'objet renvoyé à partir de cette API est réutilisable et thread-safe et peut être appelé à partir de n'importe quel thread, pas seulement du thread qui l'a récupéré. En outre, contrairement aux autres objets exposés à partir de MAPI, cet objet est valide tant que la DLL est chargée, il peut être ré-utilisé entre les sessions d'initialisation et peut être utilisé avant ou après l'appel de MAPIInitialize. Renvoie le succès ou l'échec via un HRESULT standard COM et affecte un paramètre de sortie à une instance de IMAPIInitMonitor.

```cpp
HRESULT CreateMAPIInitializationMonitor(IMAPIInitMonitor** ppInitMonitor); 
```
#### <a name="hresult-stdapicalltype-createmapiinitializationmonitorimapiinitmonitor-ppinitmonitor"></a>HRESULT STDAPICALLTYPE CreateMapiInitializationMonitor(IMAPIInitMonitor ppInitMonitor)

Ce point d'entrée exporté à partir de OLMAPI32.DLL permet à l'appelant de récupérer une interface pour interroger l'état d'initialisation actuel, configurer un rappel pour l'achèvement de l'initialisation ou bloquer le thread actuel jusqu'à ce qu'il soit terminé. L'objet renvoyé à partir de cette API est réutilisable et thread-safe et peut être appelé à partir de n'importe quel thread, pas seulement du thread qui l'a récupéré. En outre, contrairement aux autres objets exposés à partir de MAPI, cet objet est valide tant que la DLL est chargée, il peut être ré-utilisé entre les sessions d'initialisation et peut être utilisé avant ou après l'appel de MAPIInitialize. Renvoie le succès ou l'échec via un HRESULT standard COM et affecte un paramètre de sortie à une instance de IMAPIInitMonitor.
  
## <a name="quick-info"></a>Informations rapides

| identifiant | result |
|:-----|:-----|
|Exporté par :  <br/> |olmapi32.dll  <br/> |
|Appelé par :  <br/> |Client  <br/> |
|Implémenté par :  <br/> |Outlook  <br/> |

## <a name="parameters"></a>Paramètres
  
 _ppInitMonitor_
> [out] Pointeur pour recevoir l'instance nouvellement créée du moniteur d'initialisation MAPI.
  
## <a name="return-values"></a>Valeurs de retour

S_OK
> Une nouvelle instance du moniteur d'initialisation a été créée avec succès.

E_OUTOFMEMORY
> Il n'y avait pas assez de mémoire pour un nouvel objet.

## <a name="see-also"></a>Voir aussi
[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIWaitResult](imapiwaitresultiunknown.md)
