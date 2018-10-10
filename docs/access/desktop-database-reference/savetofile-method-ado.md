---
title: SaveToFile, méthode (ADO)
TOCTitle: SaveToFile Method (ADO)
ms:assetid: db0fd95e-8ef3-af87-5346-8f8713153ca7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250104(v=office.15)
ms:contentKeyID: 48548097
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c0bd915a4eb6405b7d5ddd4bfe42eb4a98f68b89
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469696"
---
# <a name="savetofile-method-ado"></a>SaveToFile, méthode (ADO)


**S’applique à**: Access 2013 | Office 2013



Enregistre le contenu binaire d'un objet [Stream](stream-object-ado.md) dans un fichier.

## <a name="syntax"></a>Syntaxe

*Flux de données*. De SaveToFile*FileName*, groupes de *SaveOptions*

## <a name="parameters"></a>Paramètres

  - *FileName*

  - Valeur de type **String** qui contient le nom complet du fichier dans lequel le contenu de l'objet **Stream** sera enregistré. Vous pouvez enregistrer dans tout emplacement local valide ou tout emplacement auquel vous avez accès via une valeur UNC.

  - *SaveOptions*

  - Valeur [SaveOptionsEnum](saveoptionsenum.md) qui spécifie si un nouveau fichier doit être créé par la méthode **SaveToFile**, s'il n'existe pas encore. La valeur par défaut est **adSaveCreateNotExists**. Avec ces options, vous pouvez déterminer qu'une erreur doit être générée lorsque le fichier spécifié n'existe pas. Vous pouvez également préciser que la méthode **SaveToFile** remplace le contenu actuel d'un fichier existant.


> [!NOTE]
> <P>[!REMARQUE] Si vous remplacez un fichier existant (lorsque la valeur <STRONG>adSaveCreateOverwrite</STRONG> est définie), la méthode <STRONG>SaveToFile</STRONG> tronque tous les octets du fichier existant d'origine qui suivent la nouvelle propriété <A href="eos-property-ado.md">EOS</A>.</P>



## <a name="remarks"></a>Notes

La méthode **SaveToFile** peut être utilisée pour copier le contenu d'un objet **Stream** vers un fichier local. Le contenu ou les propriétés de l'objet **Stream** ne sont en aucune façon modifiés. L'objet **Stream** doit être ouvert avant d'appeler **SaveToFile**.

Cette méthode ne modifie pas l'association entre l'objet **Stream** et sa source sous-jacente. L'objet **Stream** reste associé à l'URL ou à l'objet **Record** d'origine qui représentait sa source lors de son ouverture.

Après une opération **SaveToFile**, la position active ([Position](position-property-ado.md)) dans le flux est définie au début du flux (0).

