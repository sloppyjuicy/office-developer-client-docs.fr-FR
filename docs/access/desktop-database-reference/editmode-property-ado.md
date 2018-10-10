---
title: EditMode, propriété (ADO)
TOCTitle: EditMode Property (ADO)
ms:assetid: 28ca8f14-abee-ad20-9c16-11bb36b487e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249045(v=office.15)
ms:contentKeyID: 48543867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a6c8377e0fa0fc2db1ec2d376ee3c8b9f16e8c99
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25469793"
---
# <a name="editmode-property-ado"></a>EditMode, propriété (ADO)


**S’applique à**: Access 2013 | Office 2013

Indique l'état d'édition de l'enregistrement actuel.

## <a name="return-value"></a>Valeur renvoyée

Renvoie la valeur [EditModeEnum](editmodeenum.md).

## <a name="remarks"></a>Remarques

ADO gère un tampon d'édition associé à l'enregistrement actuel. Cette propriété indique si des modifications ont été apportées à ce tampon ou si un nouvel enregistrement a été créé. Utilisez la propriété **EditMode** pour déterminer l'état d'édition de l'enregistrement actuel. Vous pouvez tester jusqu'à des modifications si un processus d'édition a été interrompu et détermine si vous devez utiliser la méthode [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).

Consultez la méthode [AddNew](addnew-method-ado.md) pour une description plus détaillée de la propriété **EditMode** dans des conditions d'édition différentes.

Lorsqu’un appel à [Supprimer](delete-method-ado-recordset.md) ne supprime pas correctement l’enregistrement ou des enregistrements dans les données source (en raison de violations d’intégrité référentielle, par exemple), l' [objet Recordset](recordset-object-ado.md) reste en mode édition (**EditMode** = **adEditInProgress **). Il faut donc appeler **CancelUpdate** avant de déplacer l'enregistrement actuel (avec [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) ou [Close](close-method-ado.md), par exemple).


> [!NOTE]
> <P>[!REMARQUE] <STRONG>EditMode</STRONG> ne peut renvoyer une valeur valide que s'il existe un enregistrement actuel. <STRONG>EditMode</STRONG> renvoie une erreur si la valeur de <A href="bof-eof-properties-ado.md">BOF or EOF</A> est True ou si l'enregistrement actuel a été supprimé.</P>


