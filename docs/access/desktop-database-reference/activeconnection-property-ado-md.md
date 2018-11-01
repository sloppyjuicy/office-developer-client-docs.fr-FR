---
title: ActiveConnection, propriété (ADO MD)
TOCTitle: ActiveConnection property (ADO MD)
ms:assetid: d09f0f91-5e1d-01ed-4d83-eaf58ff718a2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250043(v=office.15)
ms:contentKeyID: 48547845
ms.date: 10/17/2018
mtps_version: v=office.15
ms.openlocfilehash: 2d2ed71f938089d3238eddee91f0c533bba266c4
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25880010"
---
# <a name="activeconnection-property-ado-md"></a>ActiveConnection, propriété (ADO MD)

**S’applique à**: Access 2013, Office 2013

Indique à quel objet [Connection](connection-object-ado.md) ADO l'ensemble de cellules ou le catalogue actif appartient actuellement.

## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de type **Variant** qui contient une chaîne définissant une connexion ou un objet **Connection**. La valeur par défaut est vide.

## <a name="remarks"></a>Notes

Vous pouvez affecter à cette propriété un objet **Connection** ADO valide ou une chaîne de connexion valide. Dans ce dernier cas, le fournisseur crée un nouvel objet **Connection** à l'aide de cette définition et ouvre la connexion.

Si vous utilisez l'argument **ActiveConnection** de la méthode [Open](open-method-ado-md.md) pour ouvrir un objet [Cellset](cellset-object-ado-md.md), la propriété **ActiveConnection** héritera de la valeur de l'argument.

Lorsque vous attribuez la valeur **Nothing** à la propriété [ActiveConnection](catalog-object-ado-md.md) d'un objet **Catalog**, vous libérez les données associées, ainsi que celles de la collection [CubeDefs](cubedefs-collection-ado-md.md) et de tous les objets [Dimension](dimension-object-ado-md.md), [Hierarchy](hierarchy-object-ado-md.md), [Level](level-object-ado-md.md) et [Member](member-object-ado-md.md) liés. La fermeture d'un objet **Connection** utilisé pour ouvrir un objet **Catalog** revient à attribuer la valeur **Nothing** à la propriété **ActiveConnection**.

La modification de la base de données par défaut de la connexion référencée par la propriété **ActiveConnection** d'un objet **Catalog** object invalide le contenu de l'objet **Catalog**.

Une erreur se produit si vous tentez de modifier la propriété **ActiveConnection** d'un objet **Cellset** ouvert.

> [!NOTE]
> Dans Visual Basic, pensez à utiliser le mot clé **Set** lors de la définition de la propriété **ActiveConnection** sur un objet **Connection** . Si vous omettez le mot clé **Set** , que vous ne définissez la propriété **ActiveConnection** égale à la propriété par défaut de l’objet **Connection** , **ConnectionString**. Le code fonctionne ; Toutefois, vous allez créer une connexion supplémentaire à la source de données, qui peut avoir une incidence sur les performances.

Lorsque vous utilisez le fournisseur de données MSOLAP, définissez comme source de données d'une chaîne de connexion un nom de serveur et affectez au catalogue initial le nom d'un catalogue de la source de données. Pour vous connecter à un fichier de cube déconnecté d'un serveur, affectez comme valeur d'emplacement le chemin d'accès complet au fichier .CUB. Dans tous les cas, attribuez au fournisseur le nom du fournisseur. Par exemple, la chaîne suivante se connecte à un catalogue intitulé « Bobs Video Store » sur un serveur dénommé « Servername » avec le fournisseur MSOLAP :

`"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"`

La chaîne suivante se connecte à un fichier de cube local situé à l’emplacement c :\\MSDASDK\\exemples\\oledb\\olap\\données\\bobsvid.cub :

`"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"`

