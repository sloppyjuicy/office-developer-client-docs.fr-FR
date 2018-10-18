---
<span data-ttu-id="36b3c-101"><<<<<<< Titre tête : TOCTitle de la propriété LockType (ADO) : propriété LockType (ADO) === titre : LockType, propriété (ADO) TOCTitle : LockType, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="36b3c-101"><<<<<<< HEAD title: LockType Property (ADO) TOCTitle: LockType Property (ADO) ======= title: LockType property (ADO) TOCTitle: LockType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="36b3c-102">Master ms:assetid : 1d2622dc-6cab-1b7f-98a8-97a41d5c047f ms:mtpsurl : https://msdn.microsoft.com/library/JJ248965(v=office.15) ms:contentKeyID : ms.date 48543589 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="36b3c-102">master ms:assetid: 1d2622dc-6cab-1b7f-98a8-97a41d5c047f ms:mtpsurl: https://msdn.microsoft.com/library/JJ248965(v=office.15) ms:contentKeyID: 48543589 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="36b3c-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="36b3c-103"><<<<<<< HEAD</span></span>
# <a name="locktype-property-ado"></a><span data-ttu-id="36b3c-104">LockType, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="36b3c-104">LockType Property (ADO)</span></span>
=======
# <a name="locktype-property-ado"></a><span data-ttu-id="36b3c-105">LockType, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="36b3c-105">LockType property (ADO)</span></span>
>>>>>>> <span data-ttu-id="36b3c-106">master</span><span class="sxs-lookup"><span data-stu-id="36b3c-106">master</span></span>


<span data-ttu-id="36b3c-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="36b3c-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="36b3c-108">Indique le type des verrous placés sur les enregistrements pendant leur modification.</span><span class="sxs-lookup"><span data-stu-id="36b3c-108">Indicates the type of locks placed on records during editing.</span></span>

<span data-ttu-id="36b3c-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="36b3c-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="36b3c-110">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="36b3c-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="36b3c-111">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="36b3c-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="36b3c-112">master</span><span class="sxs-lookup"><span data-stu-id="36b3c-112">master</span></span>

<span data-ttu-id="36b3c-p101">Définit ou renvoie une valeur [LockTypeEnum](locktypeenum.md). La valeur par défaut est **adLockReadOnly**.</span><span class="sxs-lookup"><span data-stu-id="36b3c-p101">Sets or returns a [LockTypeEnum](locktypeenum.md) value. The default value is **adLockReadOnly**.</span></span>

## <a name="remarks"></a><span data-ttu-id="36b3c-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="36b3c-115">Remarks</span></span>

<span data-ttu-id="36b3c-p102">Définissez la propriété **LockType** avant d'ouvrir un [Recordset](recordset-object-ado.md) pour spécifier le type de verrouillage que le fournisseur doit utiliser pour l'ouvrir. Lisez la propriété pour connaître le type de verrouillage utilisé sur un objet **Recordset** ouvert.</span><span class="sxs-lookup"><span data-stu-id="36b3c-p102">Set the **LockType** property before opening a [Recordset](recordset-object-ado.md) to specify what type of locking the provider should use when opening it. Read the property to return the type of locking in use on an open **Recordset** object.</span></span>

<span data-ttu-id="36b3c-p103">Les fournisseurs peuvent ne pas prendre en charge tous types de verrouillage. Si un fournisseur ne reconnaît pas le paramètre **LockType** demandé, il le remplacera par un autre type de verrouillage. Pour déterminer la fonctionnalité réelle de verrouillage disponible pour un objet **Recordset**, utilisez la méthode [Supports](supports-method-ado.md) avec **adUpdate** et **adUpdateBatch**.</span><span class="sxs-lookup"><span data-stu-id="36b3c-p103">Providers may not support all lock types. If a provider cannot support the requested **LockType** setting, it will substitute another type of locking. To determine the actual locking functionality available in a **Recordset** object, use the [Supports](supports-method-ado.md) method with **adUpdate** and **adUpdateBatch**.</span></span>

<span data-ttu-id="36b3c-p104">Le paramètre **adLockPessimistic** n'est pas pris en charge si la valeur de la propriété [CursorLocation](cursorlocation-property-ado.md) est **adUseClient**. Si la valeur spécifiée n'est pas prise en charge, aucune erreur n'est générée ; c'est le **LockType** pris en charge le plus proche qui est utilisé.</span><span class="sxs-lookup"><span data-stu-id="36b3c-p104">The **adLockPessimistic** setting is not supported if the [CursorLocation](cursorlocation-property-ado.md) property is set to **adUseClient**. If an unsupported value is set, then no error will result; the closest supported **LockType** will be used instead.</span></span>

<span data-ttu-id="36b3c-123">La propriété **LockType** est accessible en lecture et en écriture lorsque le **Recordset** est fermé et en lecture seule lorsqu' il est ouvert.</span><span class="sxs-lookup"><span data-stu-id="36b3c-123">The **LockType** property is read/write when the **Recordset** is closed and read-only when it is open.</span></span>

<span data-ttu-id="36b3c-124">**L’utilisation du Service de données à distance** Lorsqu’elle est utilisée sur un objet Recordset de côté client, la propriété **LockType** peut uniquement être définie **: adLockBatchOptimistic**.</span><span class="sxs-lookup"><span data-stu-id="36b3c-124">**Remote Data Service Usage**When used on a client-side Recordset object, the **LockType** property can only be set to **adLockBatchOptimistic**.</span></span>

