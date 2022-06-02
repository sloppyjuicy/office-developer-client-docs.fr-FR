---
title: IXPProvider IUnknown
description: IXPProvider IUnknown initialise un objet fournisseur de transport et arrête l’objet lorsqu’il n’est plus nécessaire.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IXPProvider
api_type:
- COM
ms.assetid: d5507785-c924-4981-ae80-19709ceb054d
ms.openlocfilehash: f44de84a8ceb43940d3300f148f1cf6084753d29
ms.sourcegitcommit: e2b79cc4469013a4b3705620a93aa70b88e6c996
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/02/2022
ms.locfileid: "65828016"
---
# <a name="ixpprovider--iunknown"></a>IXPProvider : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Initialise un objet fournisseur de transport et arrête l’objet quand il n’est plus nécessaire.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Objets du fournisseur de transport  <br/> |
|Implémenté par :  <br/> |Fournisseurs de transport  <br/> |
|Appelé par :  <br/> |Spouleur MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IXPProvider  <br/> |
|Type de pointeur :  <br/> |LPXPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Ordre des tables virtuelles

|Member |Description |
|:-----|:-----|
|[Arrêt](ixpprovider-shutdown.md) <br/> |Ferme un fournisseur de transport de manière ordonnée. |
|[TransportLogon](ixpprovider-transportlogon.md) <br/> |Établit une session dans laquelle une application cliente se connecte à un fournisseur de transport. |
   

