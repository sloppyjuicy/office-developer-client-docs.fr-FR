---
title: IXPProvider IUnknown
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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 0e3944a585d373cc4a0eb20f2884a13c639ff72e
ms.sourcegitcommit: 241637561d21b7752ec690b5179e72b6703eaced
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/18/2022
ms.locfileid: "63631168"
---
# <a name="ixpprovider--iunknown"></a>IXPProvider : IUnknown

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Initialise un objet fournisseur de transport et arrête l’objet lorsqu’il n’est plus nécessaire.
  
|Propriété |Valeur |
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapispi.h  <br/> |
|Exposé par :  <br/> |Objets du fournisseur de transport  <br/> |
|Implémenté par :  <br/> |Fournisseurs de transport  <br/> |
|Appelé par :  <br/> |Lepooler MAPI  <br/> |
|Identificateur d’interface :  <br/> |IID_IXPProvider  <br/> |
|Type de pointeur :  <br/> |LPXPROVIDER  <br/> |
   
## <a name="vtable-order"></a>Ordre des vtables

|Member |Description |
|:-----|:-----|
|[Arrêt](ixpprovider-shutdown.md) <br/> |Ferme un fournisseur de transport de manière ordonnée. |
|[TransportLogon](ixpprovider-transportlogon.md) <br/> |Établit une session dans laquelle une application cliente se connecte à un fournisseur de transport. |
   

