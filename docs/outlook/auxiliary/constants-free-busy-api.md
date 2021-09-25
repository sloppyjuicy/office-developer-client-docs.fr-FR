---
title: Constantes (API de libre/occupé)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Cette rubrique contient des définitions de constantes, des identificateurs de classe et des identificateurs d’interface pour l’API de libre/occupé.
ms.openlocfilehash: 429c5c5d402a8239b575271dc052dd32bf29b96f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59592822"
---
# <a name="constants-freebusy-api"></a>Constantes (API de libre/occupé)

Cette rubrique contient des définitions de constantes, des identificateurs de classe et des identificateurs d’interface pour l’API de libre/occupé.
  
## <a name="constants"></a>Constantes

|**Constante**|**Définition**|
|:-----|:-----|
|E_NOTIMPL  <br/> | *Comme défini dans le fichier d’en-tête du Kit de développement logiciel (SDK) microsoft Windows,winerror.h.*  <br/> |
|E_OUTOFMEMORY  <br/> | *Comme défini dans le fichier d Windows en-tête du SDK winerror.h.*  <br/> |
|S_FALSE  <br/> | *Comme défini dans le fichier d Windows en-tête du SDK winerror.h.*  <br/> |
|S_OK  <br/> | *Comme défini dans le fichier d Windows en-tête du SDK winerror.h.*  <br/> |
   
## <a name="interface-identifiers"></a>Identificateurs d’interface

Pour les identificateurs d’interface suivants, supposons que la macro DEFINE_GUID définie dans le fichier d’en-tête du SDK Windows guiddef.h associe le nom symbolique GUID à sa valeur.
  
{00067064-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46) ;
  
{00067066-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46) ;
  
{00067067-0000-0000-C000-000000000046}
  
DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46) ;
  

