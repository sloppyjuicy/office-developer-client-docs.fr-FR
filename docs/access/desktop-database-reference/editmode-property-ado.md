---
<<<<<<< Titre tête : TOCTitle de la propriété EditMode (ADO) : EditMode propriété (ADO) === titre : EditMode, propriété (ADO) TOCTitle : EditMode, propriété (ADO)
>>>>>>> Master ms:assetid : 28ca8f14-abee-ad20-9c16-11bb36b487e4 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249045(v=office.15) ms:contentKeyID : ms.date 48543867 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="editmode-property-ado"></a>EditMode, propriété (ADO)
=======
# <a name="editmode-property-ado"></a>EditMode, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique l'état d'édition de l'enregistrement actuel.

<<<<<<< Tête
## <a name="return-value"></a>Valeur renvoyée
=======
## <a name="return-value"></a>Valeur renvoyée
>>>>>>> master

Renvoie la valeur [EditModeEnum](editmodeenum.md).

## <a name="remarks"></a>Remarques

ADO gère un tampon d'édition associé à l'enregistrement actuel. Cette propriété indique si des modifications ont été apportées à ce tampon ou si un nouvel enregistrement a été créé. Utilisez la propriété **EditMode** pour déterminer l'état d'édition de l'enregistrement actuel. Vous pouvez tester jusqu'à des modifications si un processus d'édition a été interrompu et détermine si vous devez utiliser la méthode [Update](update-method-ado.md) ou [CancelUpdate](cancelupdate-method-ado.md).

Consultez la méthode [AddNew](addnew-method-ado.md) pour une description plus détaillée de la propriété **EditMode** dans des conditions d'édition différentes.

Lorsqu’un appel à [Supprimer](delete-method-ado-recordset.md) ne supprime pas correctement l’enregistrement ou des enregistrements dans les données source (en raison de violations d’intégrité référentielle, par exemple), l' [objet Recordset](recordset-object-ado.md) reste en mode édition (**EditMode** = **adEditInProgress **). Il faut donc appeler **CancelUpdate** avant de déplacer l'enregistrement actuel (avec [Move](move-method-ado.md), [NextRecordset](nextrecordset-method-ado.md) ou [Close](close-method-ado.md), par exemple).


> [!NOTE]
> <P>[!REMARQUE] <STRONG>EditMode</STRONG> ne peut renvoyer une valeur valide que s'il existe un enregistrement actuel. <STRONG>EditMode</STRONG> renvoie une erreur si la valeur de <A href="bof-eof-properties-ado.md">BOF or EOF</A> est True ou si l'enregistrement actuel a été supprimé.</P>


