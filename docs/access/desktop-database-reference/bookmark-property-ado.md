---
title: Bookmark, propriété (ADO)
TOCTitle: Bookmark property (ADO)
ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15)
ms:contentKeyID: 48543287
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d5052b25325007a5daca76baccf7414e0c7a43cd
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889120"
---
# <a name="bookmark-property-ado"></a><span data-ttu-id="430f7-102">Bookmark, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="430f7-102">Bookmark property (ADO)</span></span>


<span data-ttu-id="430f7-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="430f7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="430f7-104">Indique un signet qui identifie de manière unique l'enregistrement actif d'un objet [Recordset](recordset-object-ado.md) ou définit comme enregistrement actif d'un objet **Recordset** l'enregistrement identifié par un signet valide.</span><span class="sxs-lookup"><span data-stu-id="430f7-104">Indicates a bookmark that uniquely identifies the current record in a [Recordset](recordset-object-ado.md) object or sets the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="430f7-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="430f7-105">Settings and return values</span></span>

<span data-ttu-id="430f7-106">Définit ou renvoie une expression de type **Variant** qui correspond à un signet valide.</span><span class="sxs-lookup"><span data-stu-id="430f7-106">Sets or returns a **Variant** expression that evaluates to a valid bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="430f7-107">Notes</span><span class="sxs-lookup"><span data-stu-id="430f7-107">Remarks</span></span>

<span data-ttu-id="430f7-p101">Utilisez la propriété **Bookmark** pour enregistrer la position de l'enregistrement actif et revenir à cet enregistrement à tout moment. Les signets ne sont disponibles que dans les objets **Recordset** prenant en charge la fonctionnalité de signet.</span><span class="sxs-lookup"><span data-stu-id="430f7-p101">Use the **Bookmark** property to save the position of the current record and return to that record at any time. Bookmarks are available only in **Recordset** objects that support bookmark functionality.</span></span>

<span data-ttu-id="430f7-p102">Lorsque vous ouvrez un objet **Recordset**, chacun de ses enregistrements possède un signet unique. Pour enregistrer le signet de l'enregistrement actif, affectez une variable comme valeur de la propriété **Bookmark**. Pour revenir rapidement à cet enregistrement à tout moment après avoir accédé à un autre enregistrement, affectez à la propriété **Bookmark** de l'objet **Recordset** la valeur de cette variable.</span><span class="sxs-lookup"><span data-stu-id="430f7-p102">When you open a **Recordset** object, each of its records has a unique bookmark. To save the bookmark for the current record, assign the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="430f7-p103">L'utilisateur n'est peut-être pas en mesure de visualiser la valeur du signet. De même, les utilisateurs ne doivent pas s'attendre à pouvoir comparer directement des signets : deux signets renvoyant au même enregistrement peuvent avoir des valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="430f7-p103">The user may not be able to view the value of the bookmark. Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</span></span>

<span data-ttu-id="430f7-p104">Si vous utilisez la méthode [Clone](clone-method-ado.md) pour créer une copie d'un objet **Recordset**, les paramètres de la propriété **Bookmark** des objets **Recordset** d'origine et dupliqué, sont identiques et vous pouvez les utiliser de manière interchangeable. Cependant, vous ne pouvez pas utiliser des signets de différents objets **Recordset** de manière interchangeable même s'ils ont été créés à partir de la même source ou de la même commande.</span><span class="sxs-lookup"><span data-stu-id="430f7-p104">If you use the [Clone](clone-method-ado.md) method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and you can use them interchangeably. However, you cannot use bookmarks from different **Recordset** objects interchangeably, even if they were created from the same source or command.</span></span>

<span data-ttu-id="430f7-117">**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet **Recordset** de côté client, la propriété **Bookmark** est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="430f7-117">**Remote Data Service Usage**When used on a client-side **Recordset** object, the **Bookmark** property is always available.</span></span>

