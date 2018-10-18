---
<span data-ttu-id="c1317-101"><<<<<<< Titre tête : TOCTitle attributs propriété (ADO) : attributs de propriété (ADO) === titre : Attributes, propriété (ADO) TOCTitle : Attributes, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="c1317-101"><<<<<<< HEAD title: Attributes Property (ADO) TOCTitle: Attributes Property (ADO) ======= title: Attributes property (ADO) TOCTitle: Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c1317-102">Master ms:assetid : 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl : https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID : ms.date 48544716 : 18/09/2015 mtps_version : v=office.15 f1_keywords :</span><span class="sxs-lookup"><span data-stu-id="c1317-102">master ms:assetid: 4cc1f036-606e-7d4b-d270-af374e9d99fa ms:mtpsurl: https://msdn.microsoft.com/library/JJ249242(v=office.15) ms:contentKeyID: 48544716 ms.date: 09/18/2015 mtps_version: v=office.15 f1_keywords:</span></span>
- <span data-ttu-id="c1317-103">Ado210.chm1231117 f1_categories :</span><span class="sxs-lookup"><span data-stu-id="c1317-103">ado210.chm1231117 f1_categories:</span></span>
- <span data-ttu-id="c1317-104">Office.Version=v15</span><span class="sxs-lookup"><span data-stu-id="c1317-104">Office.Version=v15</span></span>
---

<span data-ttu-id="c1317-105"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="c1317-105"><<<<<<< HEAD</span></span>
# <a name="attributes-property-ado"></a><span data-ttu-id="c1317-106">Attributes, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="c1317-106">Attributes Property (ADO)</span></span>
=======
# <a name="attributes-property-ado"></a><span data-ttu-id="c1317-107">Attributes, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="c1317-107">Attributes property (ADO)</span></span>
>>>>>>> <span data-ttu-id="c1317-108">master</span><span class="sxs-lookup"><span data-stu-id="c1317-108">master</span></span>


<span data-ttu-id="c1317-109">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c1317-109">**Applies to**: Access 2013 | Office 2013</span></span>


## <a name="attributes-property"></a><span data-ttu-id="c1317-110">Attributes, propriété</span><span class="sxs-lookup"><span data-stu-id="c1317-110">Attributes Property</span></span>

<span data-ttu-id="c1317-111">Indique une ou plusieurs caractéristiques d'un objet.</span><span class="sxs-lookup"><span data-stu-id="c1317-111">Indicates one or more characteristics of an object.</span></span>

<span data-ttu-id="c1317-112"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="c1317-112"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="c1317-113">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="c1317-113">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="c1317-114">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="c1317-114">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="c1317-115">master</span><span class="sxs-lookup"><span data-stu-id="c1317-115">master</span></span>

<span data-ttu-id="c1317-116">Définit ou renvoie une valeur de type **Long**.</span><span class="sxs-lookup"><span data-stu-id="c1317-116">Sets or returns a **Long** value.</span></span>

<span data-ttu-id="c1317-p101">Pour un objet [Connection](connection-object-ado.md), la propriété **Attributes** est en lecture/écriture et sa valeur peut être la somme d'une ou de plusieurs valeurs de [XactAttributeEnum](xactattributeenum.md). La valeur par défaut est zéro (0).</span><span class="sxs-lookup"><span data-stu-id="c1317-p101">For a [Connection](connection-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of one or more [XactAttributeEnum](xactattributeenum.md) values. The default is zero (0).</span></span>

<span data-ttu-id="c1317-p102">Pour un objet [Parameter](parameter-object-ado.md), la propriété **Attributes** est en lecture/écriture et sa valeur peut être la somme d'une ou de plusieurs valeurs de [ParameterAttributesEnum](parameterattributesenum.md). La valeur par défaut est **adParamSigned**.</span><span class="sxs-lookup"><span data-stu-id="c1317-p102">For a [Parameter](parameter-object-ado.md) object, the **Attributes** property is read/write, and its value can be the sum of any one or more [ParameterAttributesEnum](parameterattributesenum.md) values. The default is **adParamSigned**.</span></span>

<span data-ttu-id="c1317-p103">Pour un objet [Field](field-object-ado.md), la propriété **Attributes** peut être la somme d'une ou de plusieurs valeurs de [FieldAttributeEnum](fieldattributeenum.md). Elle est normalement en lecture seule. Cependant, pour les nouveaux objets **Field** qui ont été ajoutés à la collection [Fields](fields-collection-ado.md) d'un objet [Record](record-object-ado.md), la propriété **Attributes** est en lecture/écriture uniquement après que la propriété [Value](value-property-ado.md) de l'objet **Field** a été spécifiée et que le nouvel objet **Field** a pu être ajouté par le fournisseur de données par un appel de la méthode [Update](update-method-ado.md) de la collection **Fields**.</span><span class="sxs-lookup"><span data-stu-id="c1317-p103">For a [Field](field-object-ado.md) object, the **Attributes** property can be the sum of one or more [FieldAttributeEnum](fieldattributeenum.md) values. It is normally read-only, However, for new **Field** objects that have been appended to the [Fields](fields-collection-ado.md) collection of a [Record](record-object-ado.md), **Attributes** is read/write only after the [Value](value-property-ado.md) property for the **Field** has been specified and the new **Field** has been successfully added by the data provider by calling the [Update](update-method-ado.md) method of the **Fields** collection.</span></span>

<span data-ttu-id="c1317-123">Pour un objet [Property](property-object-ado.md), la propriété **Attributes** est en lecture seule et sa valeur peut être la somme d'une ou plusieurs valeurs de [PropertyAttributesEnum](propertyattributesenum.md).</span><span class="sxs-lookup"><span data-stu-id="c1317-123">For a [Property](property-object-ado.md) object, the **Attributes** property is read-only, and its value can be the sum of any one or more [PropertyAttributesEnum](propertyattributesenum.md) values.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1317-124">Notes</span><span class="sxs-lookup"><span data-stu-id="c1317-124">Remarks</span></span>

<span data-ttu-id="c1317-125">Utilisez la propriété **Attributes** pour définir ou retourner les caractéristiques des objets **Connection**, **Parameter**, [Field](field-object-ado.md) ou [Property](property-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="c1317-125">Use the **Attributes** property to set or return characteristics of **Connection** objects, **Parameter** objects, [Field](field-object-ado.md) objects, or [Property](property-object-ado.md) objects.</span></span>

<span data-ttu-id="c1317-p104">Lorsque vous définissez plusieurs attributs, vous pouvez additionner les constantes appropriées. Si vous attribuez à la propriété une valeur représentant une somme qui inclut des constantes incompatibles, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="c1317-p104">When you set multiple attributes, you can sum the appropriate constants. If you set the property value to a sum including incompatible constants, an error occurs.</span></span>

<span data-ttu-id="c1317-128">**L’utilisation du Service de données à distance** Cette propriété n’est pas disponible sur un objet de **connexion** côté client.</span><span class="sxs-lookup"><span data-stu-id="c1317-128">**Remote Data Service Usage**This property is not available on a client-side **Connection** object.</span></span>

