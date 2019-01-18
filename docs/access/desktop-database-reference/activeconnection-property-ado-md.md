---
title: ActiveConnection, propriété (ADO MD)
TOCTitle: ActiveConnection property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 10/17/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 372dac11500647af75881ae6b4aee22a391a32c9
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: fr-FR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703187"
---
# <a name="activeconnection-property-ado-md"></a><span data-ttu-id="bb5d4-102">ActiveConnection, propriété (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="bb5d4-102">ActiveConnection property (ADO MD)</span></span>

<span data-ttu-id="bb5d4-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bb5d4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bb5d4-104">Indique à quel objet [Connection](connection-object-ado.md) ADO l'ensemble de cellules ou le catalogue actif appartient actuellement.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-104">Indicates to which ADO [Connection](connection-object-ado.md) object the current cellset or catalog currently belongs.</span></span>

## <a name="settings-and-return-values"></a><span data-ttu-id="bb5d4-105">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="bb5d4-105">Settings and return values</span></span>

<span data-ttu-id="bb5d4-p101">Définit ou renvoie une valeur de type **Variant** qui contient une chaîne définissant une connexion ou un objet **Connection**. La valeur par défaut est vide.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-p101">Sets or returns a **Variant** that contains a string defining a connection or **Connection** object. The default is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb5d4-108">Notes</span><span class="sxs-lookup"><span data-stu-id="bb5d4-108">Remarks</span></span>

<span data-ttu-id="bb5d4-p102">Vous pouvez affecter à cette propriété un objet **Connection** ADO valide ou une chaîne de connexion valide. Dans ce dernier cas, le fournisseur crée un nouvel objet **Connection** à l'aide de cette définition et ouvre la connexion.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-p102">You can set this property to a valid ADO **Connection** object or to a valid connection string. When this property is set to a connection string, the provider creates a new **Connection** object using this definition and opens the connection.</span></span>

<span data-ttu-id="bb5d4-111">Si vous utilisez l'argument **ActiveConnection** de la méthode [Open](open-method-ado-md.md) pour ouvrir un objet [Cellset](cellset-object-ado-md.md), la propriété **ActiveConnection** héritera de la valeur de l'argument.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-111">If you use the **ActiveConnection** argument of the [Open](open-method-ado-md.md) method to open a [Cellset](cellset-object-ado-md.md) object, the **ActiveConnection** property will inherit the value of the argument.</span></span>

<span data-ttu-id="bb5d4-p103">Lorsque vous attribuez la valeur **Nothing** à la propriété [ActiveConnection](catalog-object-ado-md.md) d'un objet **Catalog**, vous libérez les données associées, ainsi que celles de la collection [CubeDefs](cubedefs-collection-ado-md.md) et de tous les objets [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) et [Member](member-object-ado-md.md) liés. La fermeture d'un objet **Connection** utilisé pour ouvrir un objet **Catalog** revient à attribuer la valeur **Nothing** à la propriété **ActiveConnection**.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-p103">Setting the **ActiveConnection** property of a [Catalog](catalog-object-ado-md.md) object to **Nothing** releases the associated data, including data in the [CubeDefs](cubedefs-collection-ado-md.md) collection and any related [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md), and [Member](member-object-ado-md.md) objects. Closing a **Connection** object that was used to open a **Catalog** has the same effect as setting the **ActiveConnection** property to **Nothing**.</span></span>

<span data-ttu-id="bb5d4-114">La modification de la base de données par défaut de la connexion référencée par la propriété **ActiveConnection** d'un objet **Catalog** object invalide le contenu de l'objet **Catalog**.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-114">Changing the default database of the connection referenced by the **ActiveConnection** property of a **Catalog** object invalidates the contents of the **Catalog**.</span></span>

<span data-ttu-id="bb5d4-115">Une erreur se produit si vous tentez de modifier la propriété **ActiveConnection** d'un objet **Cellset** ouvert.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-115">An error will occur if you attempt to change the **ActiveConnection** property for an open **Cellset** object.</span></span>

> [!NOTE]
> <span data-ttu-id="bb5d4-116">Dans Visual Basic, pensez à utiliser le mot clé **Set** lors de la définition de la propriété **ActiveConnection** sur un objet **Connection** .</span><span class="sxs-lookup"><span data-stu-id="bb5d4-116">In Visual Basic, remember to use the **Set** keyword when setting the **ActiveConnection** property to a **Connection** object.</span></span> <span data-ttu-id="bb5d4-117">Si vous omettez le mot clé **Set** , que vous ne définissez la propriété **ActiveConnection** égale à la propriété par défaut de l’objet **Connection** , **ConnectionString**.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-117">If you omit the **Set** keyword, you will actually be setting the **ActiveConnection** property equal to the **Connection** object's default property, **ConnectionString**.</span></span> <span data-ttu-id="bb5d4-118">Le code fonctionne ; Toutefois, vous allez créer une connexion supplémentaire à la source de données, qui peut avoir une incidence sur les performances.</span><span class="sxs-lookup"><span data-stu-id="bb5d4-118">The code will work; however, you will create an additional connection to the data source, which may have negative performance implications.</span></span>

<span data-ttu-id="bb5d4-p105">Lorsque vous utilisez le fournisseur de données MSOLAP, définissez comme source de données d'une chaîne de connexion un nom de serveur et affectez au catalogue initial le nom d'un catalogue de la source de données. Pour vous connecter à un fichier de cube déconnecté d'un serveur, affectez comme valeur d'emplacement le chemin d'accès complet au fichier .CUB. Dans tous les cas, attribuez au fournisseur le nom du fournisseur. Par exemple, la chaîne suivante se connecte à un catalogue intitulé « Bobs Video Store » sur un serveur dénommé « Servername » avec le fournisseur MSOLAP :</span><span class="sxs-lookup"><span data-stu-id="bb5d4-p105">When using the MSOLAP data provider, set the data source in a connection string to a server name and set the initial catalog to the name of a catalog from the data source. To connect to a cube file that is disconnected from a server, set the location to the full path to the .CUB file. In either case, set the provider to the provider name. For example, the following string connects to a catalog named Bobs Video Store on a server named Servername with the MSOLAP Provider:</span></span>

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

<span data-ttu-id="bb5d4-123">La chaîne suivante se connecte à un fichier de cube local situé à l’emplacement c :\\MSDASDK\\exemples\\oledb\\olap\\données\\bobsvid.cub :</span><span class="sxs-lookup"><span data-stu-id="bb5d4-123">The following string connects to a local cube file at the location C:\\MSDASDK\\samples\\oledb\\olap\\data\\bobsvid.cub:</span></span>

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

