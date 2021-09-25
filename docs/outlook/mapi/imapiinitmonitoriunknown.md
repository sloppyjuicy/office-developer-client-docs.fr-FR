---
title: 'IMAPIInitMonitor : IUnknown'
manager: lindalu
26ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIInitMonitor
api_type:
- COM
ms.assetid: ad71ea65-394d-4be2-a9da-cd23099bc2cc
description: IMAPIInitMonitor
Last modified: April 27, 2021
ms.openlocfilehash: 5eaac9c74bc08b8525e21f805d68d8c0d4cb5072
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59575994"
---
# <a name="imapiinitmonitor--iunknown"></a>IMAPIInitMonitor : IUnknown

**S’applique** à : Outlook 2013 | Outlook 2016 | Outlook 2019

Parfois, une application qui utilise MAPI peut vouloir savoir quand l’initialisation est terminée. Par exemple, il possède plusieurs threads qui peuvent initialiser MAPI, ou en réponse à l’initialisation de MAPI, l’application souhaite effectuer un travail, mais ne souhaite pas toujours faire tourner la pile MAPI. Le moniteur d’initialisation fournit cette fonctionnalité via un [objet CreateMAPIInitializationMonitor.](createmapiinitializationmonitor.md)

| informations rapides | result |
|:-----|:-----|
|Hérite de :  <br/> |IUnknown  <br/> |
|Implémenté par :  <br/> | OLMAPI32.DLL <br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIInitMonitor  <br/> |

## <a name="vtable-order"></a>Ordre des vtables

| fonction | description |
|:-----|:-----|
|[IMAPIInitMonitor::IsInitialized](imapiinitmonitor-isinitialized.md) <br/> |Renvoie l’état actuel de l’initialisation MAPI.  <br/> |
|[IMAPIInitMonitor::Wait](imapiinitmonitor-wait.md) <br/> |Lance un appel BLOCKING sur ce thread, qui retourne soit lorsque le nombre de millisecondes spécifié est écoulé, soit que MAPI a été initialisé.  INFINITE peut être utilisé pour une attente infinie.  <br/> |
|[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md) <br/> |Démarrez une attente pour l’initialisation de MAPI ou le nombre spécifié de millisecondes qui s’écoulént. Cette commande retourne une interface IMAPIWaitResult qui doit avoir appelé « End » afin de commencer l’attente.  Cela permet à l’appelant de contrôler quel thread est bloqué pendant que nous sommes en attente. <br/> |

## <a name="see-also"></a>Voir aussi

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
