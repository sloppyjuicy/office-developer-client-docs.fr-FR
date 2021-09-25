---
title: 'IMAPIWaitResult : IUnknown'
manager: lindalu
ms.date: 04/27/2021
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIWAITRESULT
api_type:
- COM
ms.assetid: d7157f57-709d-4e53-973b-176954e2bb73
description: IMAPIWaitResult
Last modified: April 27, 2021
ms.openlocfilehash: 624c9e60e2ca12f280c4f754986a10aee7735b10
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584345"
---
# <a name="imapiwaitresult--iunknown"></a>IMAPIWaitResult : IUnknown
  
**S’applique** à : Outlook 2013 | Outlook 2016 | Outlook 2019

Cette interface est utilisée par les consommateurs d’IMAPIInitMonitor pour contrôler l’endroit où l’attente se produit. Il leur permet de créer l’objet sur un thread et de le déplacer sur un autre thread pour effectuer l’attente réelle.

## <a name="vtable-order"></a>Ordre des vtables

| fonction | description |
|:-----|:-----|
|[HRESULT IMAPIWaitResult::End()](imapiwaitresult-end.md)|Appelé pour lancer l’attente bloquante sur le thread où il est appelé, qui ne doit pas nécessairement être le même thread que celui appelé *IMAPIInitMonitor::BeginWait*.|

| informations rapides | result |
|:-----|:-----|
|Hérite de :  <br/> |IUnknown  <br/> |
|Implémenté par :  <br/> |  OLMAPI32.DLL<br/> |
|Appelé par :  <br/> |Applications clientes  <br/> |
|Identificateur d’interface :  <br/> |IID_IMAPIWaitResult  <br/> |

## <a name="see-also"></a>Voir aussi

[IMAPIInitMonitor](imapiinitmonitoriunknown.md)

[IMAPIInitMonitor::BeginWait](imapiinitmonitor-beginwait.md)

[IMAPIInitMonitor : IUnknown](imapiinitmonitoriunknown.md)

[CreateMAPIInitializationMonitor](createmapiinitializationmonitor.md)
