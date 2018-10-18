---
<span data-ttu-id="bde9e-101"><<<<<<< Titre tête : TOCTitle Position propriété (ADO) : Position propriété (ADO) === titre : Position, propriété (ADO) TOCTitle : Position, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="bde9e-101"><<<<<<< HEAD title: Position Property (ADO) TOCTitle: Position Property (ADO) ======= title: Position property (ADO) TOCTitle: Position property (ADO)</span></span>
>>>>>>> <span data-ttu-id="bde9e-102">Master ms:assetid : a07c9197-673b-ddf2-fca9-b0b54fbd67b4 ms:mtpsurl : https://msdn.microsoft.com/library/JJ249738(v=office.15) ms:contentKeyID : ms.date 48546709 : 18/09/2015 mtps_version : v=office.15</span><span class="sxs-lookup"><span data-stu-id="bde9e-102">master ms:assetid: a07c9197-673b-ddf2-fca9-b0b54fbd67b4 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249738(v=office.15) ms:contentKeyID: 48546709 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="bde9e-103"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="bde9e-103"><<<<<<< HEAD</span></span>
# <a name="position-property-ado"></a><span data-ttu-id="bde9e-104">Position, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="bde9e-104">Position Property (ADO)</span></span>
=======
# <a name="position-property-ado"></a><span data-ttu-id="bde9e-105">Position, propriété (ADO)</span><span class="sxs-lookup"><span data-stu-id="bde9e-105">Position property (ADO)</span></span>
>>>>>>> <span data-ttu-id="bde9e-106">master</span><span class="sxs-lookup"><span data-stu-id="bde9e-106">master</span></span>


<span data-ttu-id="bde9e-107">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bde9e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bde9e-108">Indique la position actuelle dans un objet [Stream](stream-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="bde9e-108">Indicates the current position within a [Stream](stream-object-ado.md) object.</span></span>

<span data-ttu-id="bde9e-109"><<<<<<< Tête</span><span class="sxs-lookup"><span data-stu-id="bde9e-109"><<<<<<< HEAD</span></span>
## <a name="settings-and-return-values"></a><span data-ttu-id="bde9e-110">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="bde9e-110">Settings and Return Values</span></span>
=======
## <a name="settings-and-return-values"></a><span data-ttu-id="bde9e-111">Paramètres et valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="bde9e-111">Settings and return values</span></span>
>>>>>>> <span data-ttu-id="bde9e-112">master</span><span class="sxs-lookup"><span data-stu-id="bde9e-112">master</span></span>

<span data-ttu-id="bde9e-p101">Définit ou retourne une valeur de type **Long** qui spécifie le décalage, en nombre d'octets, de la position actuelle par rapport au début du flux. La valeur par défaut est 0 ; elle représente le premier octet du flux.</span><span class="sxs-lookup"><span data-stu-id="bde9e-p101">Sets or returns a **Long** value that specifies the offset, in number of bytes, of the current position from the beginning of the stream. The default is 0, which represents the first byte in the stream.</span></span>

## <a name="remarks"></a><span data-ttu-id="bde9e-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="bde9e-115">Remarks</span></span>

<span data-ttu-id="bde9e-p102">La position actuelle peut être définie au-delà de la fin du flux. Dans ce cas, la propriété [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) de l'objet **Stream** est augmentée en conséquence. Les nouveaux octets ajoutés de cette façon sont nuls.</span><span class="sxs-lookup"><span data-stu-id="bde9e-p102">The current position can be moved to a point after the end of the stream. If you specify the current position beyond the end of the stream, the [Size](https://msdn.microsoft.com/library/jj250128\(v=office.15\)) of the **Stream** object will be increased accordingly. Any new bytes added in this way will be null.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bde9e-p103">[!REMARQUE] <STRONG>Position</STRONG> mesure toujours des octets. Pour les flux de texte utilisant des jeux de caractères multioctet, multipliez la position par la taille de caractères pour déterminer le numéro du caractère. Par exemple, dans un jeu de caractères de deux octets, le premier caractère est en position 0, le deuxième en position 2, le troisième en position 4, etc.</span><span class="sxs-lookup"><span data-stu-id="bde9e-p103"><STRONG>Position</STRONG> always measures bytes. For text streams using multibyte character sets, multiply the position by the character size to determine the character number. For example, for a two-byte character set, the first character is at position 0, the second character at position 2, the third character at position 4, and so on.</span></span></P>



<span data-ttu-id="bde9e-p104">Il est impossible d'utiliser des valeurs négatives pour modifier la position actuelle dans un **Stream**. La propriété **Position** n'accepte que les chiffres positifs.</span><span class="sxs-lookup"><span data-stu-id="bde9e-p104">Negative values cannot be used to change the current position in a **Stream**. Only positive numbers can be used for **Position**.</span></span>

<span data-ttu-id="bde9e-124">Pour les objets **Stream** en lecture seule, ADO ne renvoie pas une erreur si la **Position** est définie sur une valeur supérieure à la **taille** du **flux de données**.</span><span class="sxs-lookup"><span data-stu-id="bde9e-124">For read-only **Stream** objects, ADO will not return an error if **Position** is set to a value greater than the **Size** of the **Stream**.</span></span> <span data-ttu-id="bde9e-125">Cela ne pas modifier la taille du **flux**ou **son contenu** .</span><span class="sxs-lookup"><span data-stu-id="bde9e-125">This does not change the size of the **Stream**, or alter the **Stream** contents in any way.</span></span> <span data-ttu-id="bde9e-126">Toutefois, cette opération doit être évitée, car elle génère une valeur de **Position** sans signification.</span><span class="sxs-lookup"><span data-stu-id="bde9e-126">However, doing this should be avoided because it results in a meaningless **Position** value.</span></span>

