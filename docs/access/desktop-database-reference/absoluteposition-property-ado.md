---
<<<<<<< Titre tête : TOCTitle de la propriété AbsolutePosition (ADO) : ms:assetid de la propriété AbsolutePosition (ADO) : 500be001-9fa1-177b-f19d-acf003a0cdc2 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249259(v=office.15) ms:contentKeyID : ms.date 48544787 : mtps_ 18/09/2015 version : v=office.15
---

# <a name="absoluteposition-property-ado"></a>AbsolutePosition, propriété (ADO)

=== titre : AbsolutePosition, propriété (ADO) TOCTitle : AbsolutePosition, propriété (ADO) ms:assetid : 500be001-9fa1-177b-f19d-acf003a0cdc2 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249259(v=office.15) ms:contentKeyID : ms.date 48544787 : 17/10/2018 mtps_version : v=office.15
---

# <a name="absoluteposition-property-ado"></a>AbsolutePosition, propriété (ADO)
>>>>>>> master

**S’applique à**: Access 2013 | Office 2013

Indique la position ordinale de l'enregistrement actif de l'objet [Recordset](recordset-object-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur de type **Long** comprise entre 1 et le nombre d’enregistrements dans l’objet **Recordset** ([RecordCount](recordcount-property-ado.md)), ou renvoie l’une des valeurs de [PositionEnum](positionenum.md).

## <a name="remarks"></a>Remarques

<<<<<<< Tête de commande pour définir la propriété **AbsolutePosition** , ADO nécessite que le fournisseur OLE DB que vous utilisez doit implémenter l’interface IRowsetLocate.
=== Pour définir la propriété **AbsolutePosition** , ADO exige que le fournisseur OLE DB que vous utilisez implémente l’interface IRowsetLocate.
>>>>>>> master

L'accès à la propriété **AbsolutePosition** d'un objet **Recordset** ouvert avec un curseur dynamique ou avant uniquement génère une erreur **adErrFeatureNotAvailable**. Avec les autres types de curseur, la position correcte est retournée pour autant que le fournisseur prenne en charge l'interface IRowsetScroll. Si le fournisseur ne prend pas en charge l'interface *IRowsetScroll*, la propriété est définie sur **adPosUnknown**. Reportez-vous à la documentation pour déterminer si l'interface *IRowsetScroll* est prise en charge.

La propriété **AbsolutePosition** permet d'accéder à un enregistrement donné, en fonction de sa position ordinale dans l'objet **Recordset** ou de déterminer la position ordinale de l'enregistrement actif. Le fournisseur doit prendre en charge les fonctionnalités requises pour que cette propriété soit disponible.

Comme la propriété [AbsolutePage](absolutepage-property-ado.md), la propriété **AbsolutePosition** est en base 1 et est égale à 1 lorsque l'enregistrement actif est le premier enregistrement de l'objet **Recordset**. Vous pouvez obtenir le nombre total d'enregistrements dans l'objet **Recordset** à partir de la propriété [RecordCount](recordcount-property-ado.md).

<<<<<<< Tête lorsque vous définissez la propriété **AbsolutePosition** , même s’il s’agit un enregistrement dans le cache actif, ADO recharge le cache avec un nouveau groupe d’enregistrements commençant par l’enregistrement que vous avez spécifié. La propriété [CacheSize](cachesize-property-ado.md) détermine la taille de ce groupe.


> [!NOTE]
> <a name="pyou-should-not-use-the-strongabsolutepositionstrong-property-as-a-surrogate-record-number-the-position-of-a-given-record-changes-when-you-delete-a-preceding-record-there-is-also-no-assurance-that-a-given-record-will-have-the-same-strongabsolutepositionstrong-if-the-strongrecordsetstrong-object-is-requeried-or-reopened-bookmarks-are-still-the-recommended-way-of-retaining-and-returning-to-a-given-position-and-are-the-only-way-of-positioning-across-all-types-of-strongrecordsetstrong-objectsp"></a><P>[!REMARQUE] Vous ne devez pas utiliser la propriété <STRONG>AbsolutePosition</STRONG> comme numéro d'enregistrement de substitution. La position d'un enregistrement donné change lorsque vous supprimez un enregistrement précédent. Rien ne garantit qu'un enregistrement donné possédera la même valeur <STRONG>AbsolutePosition</STRONG> si l'objet <STRONG>Recordset</STRONG> est actualisé ou rouvert. Les signets restent le meilleur moyen de conserver et renvoyer une position donnée puisqu'ils offrent la possibilité de se positionner dans tous les types d'objets <STRONG>Recordset</STRONG>.</P>
=======
Lorsque vous définissez la propriété **AbsolutePosition** , même s’il s’agit un enregistrement dans le cache actif, ADO recharge le cache avec un nouveau groupe d’enregistrements commençant par l’enregistrement que vous avez spécifié. La propriété [CacheSize](cachesize-property-ado.md) détermine, quant à elle, la taille de ce groupe.


> [!NOTE]
> [!REMARQUE] Vous ne pouvez pas utiliser la propriété **AbsolutePosition** en tant que numéro d'enregistrement de substitution. La position d'un enregistrement donné change lorsque vous supprimez un enregistrement précédent. Rien ne garantit qu'un enregistrement donné possédera la même valeur **AbsolutePosition** si l'objet **Recordset** est actualisé ou rouvert. Signets sont toujours recommandé de conserver et renvoyer une position donnée et sont le seul moyen de se positionner dans tous les types d’objets **Recordset** .
>>>>>>> master


