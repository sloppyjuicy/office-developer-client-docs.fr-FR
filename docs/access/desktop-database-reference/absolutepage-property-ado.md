---
<<<<<<< Titre tête : TOCTitle AbsolutePage propriété (ADO) : AbsolutePage propriété (ADO) ms:assetid : b6e5daac-cc21-0aa6-9119-a973595762bb ms:mtpsurl : https://msdn.microsoft.com/library/JJ249881(v=office.15) ms:contentKeyID : ms.date 48547288 : mtps_version 18/09/2015 : v = Office.15
---

# <a name="absolutepage-property-ado"></a>AbsolutePage, propriété (ADO)

=== titre : AbsolutePage, propriété (ADO) TOCTitle : AbsolutePage, propriété (ADO) ms:assetid : b6e5daac-cc21-0aa6-9119-a973595762bb ms:mtpsurl : https://msdn.microsoft.com/library/JJ249881(v=office.15) ms:contentKeyID : ms.date 48547288 : 17/10/2018 mtps_version : v=office.15
---

# <a name="absolutepage-property-ado"></a>AbsolutePage, propriété (ADO)
>>>>>>> master

**S’applique à**: Access 2013 | Office 2013

Indique la page sur laquelle se trouve l'enregistrement actif.

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

<a name="sets-or-returns-a-long-value-from-1-to-the-number-of-pages-in-the-recordsetrecordset-object-adomd-object--pagecountpagecount-property-adomd--or-returns-one-of-the-positionenumpositionenummd-values"></a>Définit ou renvoie une valeur de type **Long** comprise entre 1 et le nombre de pages dans l'objet [Recordset](recordset-object-ado.md) ( [PageCount](pagecount-property-ado.md)), ou renvoie l'une des valeurs de [PositionEnum](positionenum.md).
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour

Définit ou renvoie une valeur de **type Long** comprise entre 1 et le nombre de pages dans l’objet [Recordset](recordset-object-ado.md) ([PageCount](pagecount-property-ado.md)) ou renvoie une des valeurs de [PositionEnum](positionenum.md) .
>>>>>>> master

## <a name="remarks"></a>Notes

Cette propriété peut être utilisée pour identifier le numéro de page sur laquelle se trouve l'enregistrement actif. Elle utilise la propriété [PageSize](pagesize-property-ado.md) pour séparer logiquement le nombre total de jeux de lignes de l'objet **Recordset** en une série de pages, chacune possédant un nombre d'enregistrements égal à **PageSize** (à l'exception de la dernière page, qui peut comporter moins d'enregistrements). Le fournisseur doit prendre en charge les fonctions appropriées pour que cette propriété soit disponible.

Lors de l'extraction ou de la définition de la propriété **AbsolutePage**, ADO utilise conjointement les propriétés [AbsolutePosition](absoluteposition-property-ado.md) et [PageSize](pagesize-property-ado.md), de la manière suivante :

<<<<<<< Tête
  - Pour extraire **AbsolutePage**, ADO commence par extraire **AbsolutePosition**, qu'il divise par la valeur **PageSize**.

  - Pour définir **AbsolutePage**, ADO déplace **AbsolutePosition** de la manière suivante : il multiplie **PageSize** par la nouvelle valeur **AbsolutePage** et y ajoute 1. En conséquence, la position active dans l'objet **Recordset**, une fois la valeur **AbsolutePage** définie, correspond au premier enregistrement de cette page.
=======
- Pour extraire **AbsolutePage**, ADO commence par extraire **AbsolutePosition**, qu'il divise par la valeur **PageSize**.

- Pour définir **AbsolutePage**, ADO déplace **AbsolutePosition** de la manière suivante : il multiplie **PageSize** par la nouvelle valeur **AbsolutePage** et y ajoute 1. Par conséquent, la position actuelle dans le **jeu d’enregistrements** une fois la valeur **AbsolutePage** est le premier enregistrement de cette page.
>>>>>>> master

Comme la propriété **AbsolutePosition**, la propriété **AbsolutePage** est en base 1 et est égale à 1 lorsque l'enregistrement actif correspond au premier enregistrement du **Recordset**. Définissez cette propriété pour accéder au premier enregistrement d'une page déterminée. Obtenez le nombre total de pages à partir de la propriété **PageCount**.

