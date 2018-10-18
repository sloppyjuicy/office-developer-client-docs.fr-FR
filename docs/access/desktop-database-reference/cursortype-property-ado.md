---
<span data-ttu-id="27bda-101"><<<<<<< Titre tête : propriété CursorType (ADO) TOCTitle : propriété CursorType (ADO) === titre : CursorType, propriété (ADO) TOCTitle : CursorType, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="27bda-101"><<<<<<< HEAD title: CursorType Property (ADO) TOCTitle: CursorType Property (ADO) ======= title: CursorType property (ADO) TOCTitle: CursorType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="27bda-102">Master ms:assetid : f42ded8f-9f92-ef03-a198-ffb892324611 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250239(v=office.15) ms:contentKeyID : ms.date 48548682 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="27bda-102">master ms:assetid: f42ded8f-9f92-ef03-a198-ffb892324611 ms:mtpsurl: https://msdn.microsoft.com/library/JJ250239(v=office.15) ms:contentKeyID: 48548682 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="27bda-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="27bda-103"><<<<<<< HEAD</span></span>
# <a name="cursortype-property-ado"></a><span data-ttu-id="27bda-104">CursorType, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="27bda-104">CursorType Property (ADO)</span></span>
=======
# <a name="cursortype-property-ado"></a><span data-ttu-id="27bda-105">CursorType, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="27bda-105">CursorType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="27bda-106">master</span><span class="sxs-lookup"><span data-stu-id="27bda-106">master</span></span>


<span data-ttu-id="27bda-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="27bda-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="27bda-108">Indique le type de curseur utilisé dans un objet [Recordset](recordset-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="27bda-108">Indicates the type of cursor used in a [Recordset](recordset-object-ado.md) object.</span></span>

<span data-ttu-id="27bda-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="27bda-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="27bda-110">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="27bda-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="27bda-111">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="27bda-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="27bda-112">master</span><span class="sxs-lookup"><span data-stu-id="27bda-112">master</span></span>

<span data-ttu-id="27bda-p101">Définit ou retourne une valeur de [CursorTypeEnum](cursortypeenum.md). La valeur par défaut est **adOpenForwardOnly**.</span><span class="sxs-lookup"><span data-stu-id="27bda-p101">Sets or returns a [CursorTypeEnum](cursortypeenum.md) value. The default value is **adOpenForwardOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="27bda-115">Notes</span><span class="sxs-lookup"><span data-stu-id="27bda-115">Remarks</span></span>

<span data-ttu-id="27bda-116">Utilisez la propriété **CursorType** pour spécifier le type de curseur à utiliser à l'ouverture de l'objet **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="27bda-116">Use the **CursorType** property to specify the type of cursor that should be used when opening the **Recordset** object.</span></span>

<span data-ttu-id="27bda-p102">Seule la valeur **adOpenStatic** est prise en charge si la propriété [CursorLocation](cursorlocation-property-ado.md) a la valeur **adUseClient**. Si une valeur non prise en charge est définie, aucune erreur n'est générée et le type de curseur ( **CursorType** ) le plus similaire pris en charge est utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="27bda-p102">Only a setting of **adOpenStatic** is supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **CursorType** will be used instead.</span></span>

<span data-ttu-id="27bda-p103">Si un fournisseur ne prend pas en charge le type de curseur demandé, il peut renvoyer un autre type de curseur. La propriété **CursorType** change pour s'adapter au type de curseur utilisé à l'ouverture de l'objet [Recordset](recordset-object-ado.md). Pour vérifier les fonctionnalités spécifiques du curseur retourné, utilisez la méthode [Supports](supports-method-ado.md). Une fois que vous fermez l'objet **Recordset**, la propriété **CursorType** reprend sa valeur initiale.</span><span class="sxs-lookup"><span data-stu-id="27bda-p103">If a provider does not support the requested cursor type, it may return another cursor type. The **CursorType** property will change to match the actual cursor type in use when the [Recordset](recordset-object-ado.md) object is open. To verify specific functionality of the returned cursor, use the [Supports](supports-method-ado.md) method. After you close the **Recordset**, the **CursorType** property reverts to its original setting.</span></span>

<span data-ttu-id="27bda-123">Le tableau ci-après indique les fonctionnalités des fournisseurs (identifiées par les constantes de la méthode **Supports** ) nécessaires à chaque type de curseur.</span><span class="sxs-lookup"><span data-stu-id="27bda-123">The following chart shows the provider functionality (identified by **Supports** method constants) required for each cursor type.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27bda-124">Pour un jeu d'enregistrements de ce type de curseur</span><span class="sxs-lookup"><span data-stu-id="27bda-124">For a Recordset of this CursorType</span></span></p></th>
<th><p><span data-ttu-id="27bda-125">La méthode Supports doit renvoyer la valeur True pour toutes ces constantes</span><span class="sxs-lookup"><span data-stu-id="27bda-125">The Supports method must return True for all of these constants</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27bda-126"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="27bda-126"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p><span data-ttu-id="27bda-127">aucune</span><span class="sxs-lookup"><span data-stu-id="27bda-127">none</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27bda-128"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="27bda-128"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p><span data-ttu-id="27bda-129"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="27bda-129"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27bda-130"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="27bda-130"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p><span data-ttu-id="27bda-131"><strong>adMovePrevious</strong></span><span class="sxs-lookup"><span data-stu-id="27bda-131"><strong>adMovePrevious</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27bda-132"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="27bda-132"><strong>adOpenStatic</strong></span></span></p></td>
<td><p><span data-ttu-id="27bda-133"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span><span class="sxs-lookup"><span data-stu-id="27bda-133"><strong>adBookmark</strong>, <strong>adHoldRecords</strong>, <strong>adMovePrevious</strong>, <strong>adResync</strong></span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="27bda-p104">Même si la méthode <STRONG>Supports</STRONG>(<STRONG>adUpdateBatch</STRONG>) peut avoir la valeur True pour les curseurs dynamiques ou avant uniquement, vous devez, pour les mises à jour par lot, utiliser un curseur de jeu de clés ou statique. Affectez à la propriété <A href="locktype-property-ado.md">LockType</A> la valeur <STRONG>adLockBatchOptimistic</STRONG> et à la propriété <STRONG>CursorLocation</STRONG> la valeur <STRONG>adUseClient</STRONG> pour activer le service de curseur pour OLE DB, nécessaire aux mises à jour par lot.</span><span class="sxs-lookup"><span data-stu-id="27bda-p104">Although <STRONG>Supports</STRONG>(<STRONG>adUpdateBatch</STRONG>) may be true for dynamic and forward-only cursors, for batch updates you should use either a keyset or static cursor. Set the <A href="locktype-property-ado.md">LockType</A> property to <STRONG>adLockBatchOptimistic</STRONG> and the <STRONG>CursorLocation</STRONG> property to <STRONG>adUseClient</STRONG> to enable the Cursor Service for OLE DB, which is required for batch updates.</span></span></P>



<span data-ttu-id="27bda-136">La propriété **CursorType** est en lecture/écriture lorsque l'objet **Recordset** est fermé et en lecture seule lorsqu'il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="27bda-136">The **CursorType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="27bda-137">**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet Recordset de côté client, la propriété **CursorType** peut avoir uniquement aux **adOpenStatic**.</span><span class="sxs-lookup"><span data-stu-id="27bda-137">**Remote Data Service Usage**When used on a client-side Recordset object, the **CursorType** property can be set only to **adOpenStatic**.</span></span>

