---
title: Property Object (DAO)
TOCTitle: Property Object
ms:assetid: a1ecb0db-bb93-a7b5-23c3-0b73f275dfe0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820932(v=office.15)
ms:contentKeyID: 48546744
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 50f7cc2b977b25602e8aec440796f105055a7437
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875630"
---
# <a name="property-object-dao"></a>Property Object (DAO)


**S’applique à**: Access 2013, Office 2013

Un objet **Property** représente une caractéristique prédéfinie ou définie par l'utilisateur d'un objet DAO.

## <a name="remarks"></a>Remarques

À l'exception des objets **Connection** et **Error**, chaque objet DAO intègre une collection **Properties** qui contient des objets **Property** correspondant à des propriétés prédéfinies de cet objet DAO. L'utilisateur peut également définir des objets **Property** et les ajouter à la collection **Properties** de certains objets DAO. Ces objets **Property** (qui sont souvent appelés propriétés) caractérisent de façon unique cette instance de l'objet.

Vous pouvez créer des propriétés définies par l'utilisateur pour les objets suivants :

  - objets **Database**, **Index**, **QueryDef** et **TableDef**;

  - objets **Field** dans les collections **Fields** d'objets **QueryDef** et **TableDef**.

Pour ajouter une propriété définie par l'utilisateur, utilisez la méthode **CreateProperty** pour créer un objet **Property** en fonction d'un paramètre de propriété **Name** unique. Définissez les propriétés **Type** et **Value** du nouvel objet **Property**, puis ajoutez-le à la collection **Properties** de l'objet approprié. L'objet auquel vous ajoutez la propriété définie par l'utilisateur doit déjà avoir été ajouté à une collection. La référence d'un objet **Property** défini par l'utilisateur qui n'a pas encore été ajouté à une collection **Properties** entraîne une erreur, de même que l'ajout d'un objet **Property** défini par l'utilisateur à une collection **Properties** contenant un objet **Property** du même nom.

Vous pouvez supprimer les propriétés définies par l'utilisateur de la collection **Properties**, mais vous ne pouvez pas supprimer les propriétés prédéfinies.


> [!NOTE]
> <P>[!REMARQUE] Un objet <STRONG>Property</STRONG> défini par l'utilisateur est associé uniquement à l'instance spécifique d'un objet. La propriété n'est pas définie pour toutes les instances d'objets du type sélectionné.</P>



Vous pouvez utiliser la collection **Properties** d'un objet pour énumérer les propriétés prédéfinies et définies par l'utilisateur de l'objet. Vous ne devez pas connaître au préalable les propriétés exactes existantes ou leurs caractéristiques (propriétés **Name** et **Type**) pour les manipuler. Toutefois, une erreur se produit lorsque vous tentez de lire une propriété en écriture seule (propriété **Password** d'un objet **Workspace**, par exemple) ou de lire ou d'écrire une propriété dans un contexte inapproprié, comme le paramètre de propriété **Value** d'un objet **Field** dans la collection **Fields** d'un objet **TableDef**.

En outre, l'objet **Property** intègre quatre propriétés prédéfinies :

  - la propriété **Name**, une valeur de type **String** qui identifie de façon unique la propriété ;

  - la propriété **Type**, une valeur de type **Integer** qui spécifie le type de données de la propriété ;

  - la propriété **Value**, une valeur de type **Variant** qui contient la valeur de propriété ;

  - la propriété **Inherited**, une valeur de type **Boolean** qui indique si la propriété est héritée d'un autre objet. Par exemple, un objet **Field** dans une collection **Fields** d'un objet **Recordset** peut hériter des propriétés issues de l'objet **TableDef** ou **QueryDef** sous-jacent.

Pour faire référence à un objet **Property** dans une collection par son numéro ordinal ou par son paramètre de propriété **Name**, utilisez l'une des formes de syntaxe suivantes :

  - * objet ***. Propriétés**(0)

  - *objet ***. Propriétés**(«* nom * »)

  - *objet ***. Propriétés**\!* nom *\]

Pour une propriété intégrée, vous pouvez également utiliser la syntaxe suivante :

  - *objet*. *nom*


> [!NOTE]
> <P>Pour une propriété définie par l’utilisateur, vous devez utiliser le complet de l' <EM>objet</EM><STRONG>. Propriétés</STRONG>syntaxe («<EM>nom</EM>»).</P>



Avec les mêmes formes de syntaxe, vous pouvez également faire référence à la propriété **Value** d'un objet **Property**. C'est le contexte de la référence qui indique si vous faites référence à l'objet **Property** ou à la propriété **Value** de l'objet **Property**.

