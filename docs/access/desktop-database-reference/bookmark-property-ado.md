---
<span data-ttu-id="bd6e8-101"><<<<<<< Titre tête : TOCTitle signet propriété (ADO) : signet propriété (ADO) === titre : Bookmark, propriété (ADO) TOCTitle : Bookmark, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd6e8-101"><<<<<<< HEAD title: Bookmark Property (ADO) TOCTitle: Bookmark Property (ADO) ======= title: Bookmark property (ADO) TOCTitle: Bookmark property (ADO)</span></span>
>>>>>>> <span data-ttu-id="bd6e8-102">Master ms:assetid : 101b2ce1-21d8-aa79-e530-20f9d1c73fc8 ms:mtpsurl : https://msdn.microsoft.com/library/JJ248870(v=office.15) ms:contentKeyID : ms.date 48543287 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="bd6e8-102">master ms:assetid: 101b2ce1-21d8-aa79-e530-20f9d1c73fc8 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248870(v=office.15) ms:contentKeyID: 48543287 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="bd6e8-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="bd6e8-103"><<<<<<< HEAD</span></span>
# <a name="bookmark-property-ado"></a><span data-ttu-id="bd6e8-104">Bookmark, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd6e8-104">Bookmark Property (ADO)</span></span>
=======
# <a name="bookmark-property-ado"></a><span data-ttu-id="bd6e8-105">Bookmark, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="bd6e8-105">Bookmark property (ADO)</span></span>
>>>>>>> <span data-ttu-id="bd6e8-106">master</span><span class="sxs-lookup"><span data-stu-id="bd6e8-106">master</span></span>


<span data-ttu-id="bd6e8-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd6e8-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bd6e8-108">Indique un signet qui identifie de manière unique l'enregistrement actif d'un objet [Recordset](recordset-object-ado.md) ou définit comme enregistrement actif d'un objet **Recordset** l'enregistrement identifié par un signet valide.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-108">Indicates a bookmark that uniquely identifies the current record in a [Recordset](recordset-object-ado.md) object or sets the current record in a **Recordset** object to the record identified by a valid bookmark.</span></span>

<span data-ttu-id="bd6e8-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="bd6e8-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="bd6e8-110">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="bd6e8-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="bd6e8-111">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="bd6e8-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="bd6e8-112">master</span><span class="sxs-lookup"><span data-stu-id="bd6e8-112">master</span></span>

<span data-ttu-id="bd6e8-113">Définit ou renvoie une expression de type **Variant** qui correspond à un signet valide.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-113">Sets or returns a **Variant** expression that evaluates to a valid bookmark.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd6e8-114">Notes</span><span class="sxs-lookup"><span data-stu-id="bd6e8-114">Remarks</span></span>

<span data-ttu-id="bd6e8-p101">Utilisez la propriété **Bookmark** pour enregistrer la position de l'enregistrement actif et revenir à cet enregistrement à tout moment. Les signets ne sont disponibles que dans les objets **Recordset** prenant en charge la fonctionnalité de signet.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-p101">Use the **Bookmark** property to save the position of the current record and return to that record at any time. Bookmarks are available only in **Recordset** objects that support bookmark functionality.</span></span>

<span data-ttu-id="bd6e8-p102">Lorsque vous ouvrez un objet **Recordset**, chacun de ses enregistrements possède un signet unique. Pour enregistrer le signet de l'enregistrement actif, affectez une variable comme valeur de la propriété **Bookmark**. Pour revenir rapidement à cet enregistrement à tout moment après avoir accédé à un autre enregistrement, affectez à la propriété **Bookmark** de l'objet **Recordset** la valeur de cette variable.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-p102">When you open a **Recordset** object, each of its records has a unique bookmark. To save the bookmark for the current record, assign the value of the **Bookmark** property to a variable. To quickly return to that record at any time after moving to a different record, set the **Recordset** object's **Bookmark** property to the value of that variable.</span></span>

<span data-ttu-id="bd6e8-p103">L'utilisateur n'est peut-être pas en mesure de visualiser la valeur du signet. De même, les utilisateurs ne doivent pas s'attendre à pouvoir comparer directement des signets : deux signets renvoyant au même enregistrement peuvent avoir des valeurs différentes.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-p103">The user may not be able to view the value of the bookmark. Also, users should not expect bookmarks to be directly comparable — two bookmarks that refer to the same record may have different values.</span></span>

<span data-ttu-id="bd6e8-p104">Si vous utilisez la méthode [Clone](clone-method-ado.md) pour créer une copie d'un objet **Recordset**, les paramètres de la propriété **Bookmark** des objets **Recordset** d'origine et dupliqué, sont identiques et vous pouvez les utiliser de manière interchangeable. Cependant, vous ne pouvez pas utiliser des signets de différents objets **Recordset** de manière interchangeable même s'ils ont été créés à partir de la même source ou de la même commande.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-p104">If you use the [Clone](clone-method-ado.md) method to create a copy of a **Recordset** object, the **Bookmark** property settings for the original and the duplicate **Recordset** objects are identical and you can use them interchangeably. However, you cannot use bookmarks from different **Recordset** objects interchangeably, even if they were created from the same source or command.</span></span>

<span data-ttu-id="bd6e8-124">**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet **Recordset** de côté client, la propriété **Bookmark** est toujours disponible.</span><span class="sxs-lookup"><span data-stu-id="bd6e8-124">**Remote Data Service Usage**When used on a client-side **Recordset** object, the **Bookmark** property is always available.</span></span>

