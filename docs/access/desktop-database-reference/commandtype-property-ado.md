---
<<<<<<< Titre tête : TOCTitle de la propriété CommandType (ADO) : CommandType propriété (ADO) === titre : CommandType, propriété (ADO) TOCTitle : CommandType, propriété (ADO)
>>>>>>> Master ms:assetid : c8d4fc1c-502b-11f3-af9d-605a03b6f056 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249976(v=office.15) ms:contentKeyID : ms.date 48547663 : 18/09/2015 mtps_version : v=office.15 f1_keywords :
- Ado210.chm1231125 f1_categories :
- Office.Version=v15
---

<<<<<<< EN-TÊTE
# <a name="commandtype-property-ado"></a>CommandType, propriété (ADO)
=======
# <a name="commandtype-property-ado"></a>CommandType, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique le type d'un objet [Command](command-object-ado.md).

<<<<<<< EN-TÊTE
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une ou plusieurs valeurs [CommandTypeEnum](commandtypeenum.md).

> [!NOTE]
> [!REMARQUE] N'utilisez pas les valeurs **CommandTypeEnum** **adCmdFile** ou **adCmdTableDirect** avec la propriété **CommandType**. Ces valeurs peuvent être uniquement utilisées en tant qu'options avec les méthodes [Open](open-method-ado-recordset.md) et [Requery](requery-method-ado.md) d'un objet [Recordset](recordset-object-ado.md).


## <a name="remarks"></a>Notes

Utilisez la propriété **CommandType** pour optimiser l'évaluation de la propriété [CommandText](commandtext-property-ado.md).

<<<<<<< Tête si la valeur de la propriété **CommandType** est égale à **adCmdUnknown** (valeur par défaut), vous pouvez rencontrer des performances car ADO doit effectuer des appels au fournisseur pour déterminer si le **CommandText** propriété est une instruction SQL, une procédure stockée ou un nom de table. Si vous connaissez le type de commande utilisé, la définition de la propriété **CommandType** permet à ADO d'accéder directement au code approprié. Si la propriété **CommandType** ne correspond pas au type de commande dans la propriété **CommandText**, une erreur se produit lorsque vous appelez la méthode [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)).
=== Si la valeur de la propriété **CommandType** est égale à **adCmdUnknown** (valeur par défaut), vous pouvez rencontrer des performances car ADO doit effectuer des appels au fournisseur pour déterminer si la propriété **CommandText** est une instruction SQL, un procédure stockée ou un nom de table. Si vous connaissez le type de commande utilisé, la définition de la propriété **CommandType** permet à ADO d'accéder directement au code approprié. Si la propriété **CommandType** ne correspond pas au type de commande dans la propriété **CommandText**, une erreur se produit lorsque vous appelez la méthode [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command).
>>>>>>> master

