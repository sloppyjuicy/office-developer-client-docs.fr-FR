---
title: Constantes (API de disponibilité)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Cette rubrique contient des définitions de constantes, des identificateurs de classe et des identificateurs d'interface pour l'API de disponibilité.
ms.openlocfilehash: 13578617eaab45e7194d7a0d4d6995ef925e7f20
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317716"
---
# <a name="constants-freebusy-api"></a>Constantes (API de disponibilité)

Cette rubrique contient des définitions de constantes, des identificateurs de classe et des identificateurs d'interface pour l'API de disponibilité.
  
## <a name="constants"></a>Constantes

|**Constante**|**Définition**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Tel que défini dans le fichier d'en-tête du kit de développement logiciel (SDK) de Microsoft Windows winerror. h.*  <br/> |
|STANDARD  <br/> | *Comme défini dans le fichier d'en-tête winerror. h du kit de développement logiciel (SDK) Windows.*  <br/> |
|S_FALSE  <br/> | *Comme défini dans le fichier d'en-tête winerror. h du kit de développement logiciel (SDK) Windows.*  <br/> |
|S_OK  <br/> | *Comme défini dans le fichier d'en-tête winerror. h du kit de développement logiciel (SDK) Windows.*  <br/> |
   
## <a name="interface-identifiers"></a>Identificateurs d’interface

Pour les identificateurs d'interface suivants, supposons que la macro DEFINE_GUID définie dans le fichier d'en-tête du kit de développement logiciel (SDK) Windows guiddef. h associe le nom symbolique du GUID à sa valeur.
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xC0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);
  

