---
title: EditMode, propriété (ADO)
TOCTitle: EditMode property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7d7bba0af804df89bf4c8611e184928c9bf12d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293608"
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


