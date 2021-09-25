---
title: EditMode, propriété (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 50fe7a1c034e1e60863ee04da523f41bb7eadb46
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581405"
---
# <a name="editmode-property-ado"></a>EditMode, propriété (ADO)


**S’applique à** : Access 2013, Office 2013

Indique l'état d'édition de l'enregistrement actuel.

## <a name="return-value"></a>Valeur renvoyée

Renvoie la valeur [EditModeEnum](editmodeenum.md).

## <a name="remarks"></a>Remarques

ADO gère un tampon d'édition associé à l'enregistrement actuel. Cette propriété indique si des modifications ont été apportées à ce tampon ou si un nouvel enregistrement a été créé. Utilisez la propriété **EditMode** pour déterminer l'état d'édition de l'enregistrement actuel. Vous pouvez tester jusqu'à des modifications si un processus d'édition a été interrompu et détermine si vous devez utiliser la méthode [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).

Consultez la méthode [AddNew](addnew-method-ado.md) pour une description plus détaillée de la propriété **EditMode** dans des conditions d'édition différentes.

Lorsqu’un [](delete-method-ado-recordset.md) appel à la suppression ne supprime pas correctement l’enregistrement ou les enregistrements dans [](recordset-object-ado.md) la source de données (en raison de violations d’intégrité référence, par exemple), le jeu d’enregistrements reste en mode édition (**EditMode**  =  **adEditInProgress**). Il faut donc appeler **CancelUpdate** avant de déplacer l'enregistrement actuel (avec [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) ou [Close](close-method-ado.md), par exemple).


> [!NOTE]
> [!REMARQUE] **EditMode** ne peut renvoyer une valeur valide que s'il existe un enregistrement actuel. **EditMode** renvoie une erreur si la valeur de [BOF or EOF](bof-eof-properties-ado.md) est True ou si l'enregistrement actuel a été supprimé.


