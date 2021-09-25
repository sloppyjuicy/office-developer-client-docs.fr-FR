---
title: SaveToFile, méthode (ADO)
TOCTitle: SaveToFile method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 49ef7e94d0e196436500d0180a05a2e475660cfc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59589175"
---
# <a name="savetofile-method-ado"></a>SaveToFile, méthode (ADO)

**S’applique à** : Access 2013, Office 2013

Enregistre le contenu binaire d’un objet [Stream](stream-object-ado.md) dans un fichier.

## <a name="syntax"></a>Syntaxe

*Stream*. SaveToFile *FileName*, *SaveOptions*

## <a name="parameters"></a>Paramètres

|Paramètre|Description|
|:--------|:----------|
|*FileName* |Valeur de type **String** qui contient le nom complet du fichier dans lequel le contenu de l'objet **Stream** sera enregistré. Vous pouvez enregistrer dans tout emplacement local valide ou tout emplacement auquel vous avez accès via une valeur UNC.|
|*SaveOptions* |Valeur [SaveOptionsEnum](saveoptionsenum.md) qui spécifie si un nouveau fichier doit être créé par la méthode **SaveToFile**, s'il n'existe pas encore. La valeur par défaut est **adSaveCreateNotExists**. Avec ces options, vous pouvez déterminer qu'une erreur doit être générée lorsque le fichier spécifié n'existe pas. Vous pouvez également préciser que la méthode **SaveToFile** remplace le contenu actuel d'un fichier existant.|

> [!NOTE]
> Si vous remplacez un fichier existant (lorsque la valeur **adSaveCreateOverwrite** est définie), la méthode **SaveToFile** tronque tous les octets du fichier existant d’origine qui suivent la nouvelle propriété [EOS](eos-property-ado.md).

## <a name="remarks"></a>Remarques

La méthode **SaveToFile** peut être utilisée pour copier le contenu d'un objet **Stream** vers un fichier local. Le contenu ou les propriétés de l'objet **Stream** ne sont en aucune façon modifiés. L'objet **Stream** doit être ouvert avant d'appeler **SaveToFile**.

Cette méthode ne modifie pas l'association entre l'objet **Stream** et sa source sous-jacente. L'objet **Stream** reste associé à l'URL ou à l'objet **Record** d'origine qui représentait sa source lors de son ouverture.

Après une opération **SaveToFile**, la position active ([Position](position-property-ado.md)) dans le flux est définie au début du flux (0).

