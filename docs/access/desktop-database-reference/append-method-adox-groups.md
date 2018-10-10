---
title: Append, méthode (Groupes ADOX)
TOCTitle: Append Method (ADOX Groups)
ms:assetid: c3245a24-55b8-3f3f-1c4a-43a119d84dc8
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249954(v=office.15)
ms:contentKeyID: 48547567
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 76c602896a629881d06a3f3cf80326e02340186e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25472133"
---
# <a name="append-method-adox-groups"></a>Append, méthode (Groupes ADOX)


**S’applique à**: Access 2013 | Office 2013



Ajoute un nouvel objet [Group](group-object-adox.md) à la collection [Groups](groups-collection-adox.md).

## <a name="syntax"></a>Syntaxe

*Groupes*. Ajouter le*groupe*

## <a name="parameters"></a>Paramètres

  - *Group*

  - Objet **Group** à ajouter ou nom du groupe à créer et à ajouter.

## <a name="remarks"></a>Notes

La collection **Groups** d'un objet [Catalog](catalog-object-adox.md) représente tous les comptes de groupe du catalogue. La collection **Groups** d'un objet [User](user-object-adox.md) contient uniquement le groupe auquel l'utilisateur appartient.

Une erreur se produit si le fournisseur ne prend pas en charge la création de groupes.


> [!NOTE]
> <P>[!REMARQUE] Avant d'ajouter un objet <STRONG>Group</STRONG> à la collection <STRONG>Groups</STRONG> d'un objet <STRONG>User</STRONG>, un objet <STRONG>Group</STRONG> affecté de la même propriété <A href="name-property-adox.md">Name</A> que celui à ajouter doit déjà exister dans la collection <STRONG>Groups</STRONG> de l'objet <STRONG>Catalog</STRONG>.</P>


