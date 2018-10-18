---
<<<<<<< Titre tête : valeur propriété (ADO) TOCTitle : valeur de propriété (ADO) === titre : Value, propriété (ADO) TOCTitle : Value, propriété (ADO)
>>>>>>> Master ms:assetid : ff21d122-98e3-2b48-d92f-e696b8079fc5 ms:mtpsurl : https://msdn.microsoft.com/library/JJ250310(v=office.15) ms:contentKeyID : ms.date 48548958 : 18/09/2015 mtps_version : v=office.15
---

<<<<<<< Tête
# <a name="value-property-ado"></a>Value, propriété (ADO)
=======
# <a name="value-property-ado"></a>Value, propriété (ADO)
>>>>>>> master


**S’applique à**: Access 2013 | Office 2013

Indique la valeur attribuée à un objet [Field](field-object-ado.md), [Parameter](parameter-object-ado.md) ou [Property](property-object-ado.md).

<<<<<<< Tête
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
=======
## <a name="settings-and-return-values"></a>Paramètres et valeurs de retour
>>>>>>> master

Définit ou renvoie une valeur **Variant** qui indique la valeur de l'objet. La valeur par défaut dépend de la propriété [Type](type-property-ado.md).

## <a name="remarks"></a>Remarques

Utilisez la propriété **Valeur** pour définir ou renvoyer des données d'objets **Field**, pour définir ou renvoyer des valeurs de paramètres avec les objets **Parameter** ou pour définir ou renvoyer des paramètres de propriété avec les objets **Property**. La propriété **Value** peut être en lecture/écriture ou en lecture seule ; cela dépend de nombreux facteurs (voir les rubriques sur les objets concernés pour plus d'informations).

ADO permet de définir et de renvoyer des données binaires longues avec la propriété **Value**.


> [!NOTE]
> <P>[!REMARQUE] Pour les objets <STRONG>Parameter</STRONG>, ADO lit la propriété <STRONG>Value</STRONG> une seule fois à partir du fournisseur. Si une commande contient un objet <STRONG>Parameter</STRONG> dont la propriété <STRONG>Value</STRONG> est vide et que vous créez un <A href="recordset-object-ado.md">Recordset</A> à partir de la commande, veillez à fermer le <STRONG>Recordset</STRONG> avant d'extraire la propriété <STRONG>Value</STRONG>. Sinon, pour certains fournisseurs, la propriété <STRONG>Value</STRONG> risque d'être vide ou de ne pas contenir la bonne valeur.</P>



Pour les nouveaux objets **Field** ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), la propriété **Value** doit être définie avant les propriétés **Field**. Il faut d'abord attribuer une valeur spécifique à la propriété **Value** et appeler [Update](update-method-ado.md) sur la collection **Fields**. Il sera alors possible d'accéder aux autres propriétés comme [Type](type-property-ado.md) ou [Attributes](attributes-property-ado.md).

