---
title: DBEngine.DefaultUser Property (DAO)
TOCTitle: DefaultUser Property
ms:assetid: 41ee0211-0794-6026-7341-3698a0b2c588
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192905(v=office.15)
ms:contentKeyID: 48544464
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053071
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 15fc13b27b30c87bd3993b12303cc59b8a0115bf
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/09/2018
ms.locfileid: "25470000"
---
# <a name="dbenginedefaultuser-property-dao"></a><span data-ttu-id="c2634-102">DBEngine.DefaultUser Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="c2634-102">DBEngine.DefaultUser Property (DAO)</span></span>


<span data-ttu-id="c2634-103">**S’applique à**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2634-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c2634-p101">Définit le nom d'utilisateur servant à créer l'objet **Workspace** par défaut lors de son initialisation. Valeur de type **String** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="c2634-p101">Sets the user name used to create the default **Workspace** when it is initialized. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2634-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2634-106">Syntax</span></span>

<span data-ttu-id="c2634-107">*expression* . DefaultUser</span><span class="sxs-lookup"><span data-stu-id="c2634-107">*expression* .DefaultUser</span></span>

<span data-ttu-id="c2634-108">*expression* Expression qui renvoie un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="c2634-108">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2634-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="c2634-109">Remarks</span></span>

<span data-ttu-id="c2634-110">Le paramètre de la **propriété DefaultUser** est un type de données String.</span><span class="sxs-lookup"><span data-stu-id="c2634-110">The setting for **DefaultUser** is a String data type.</span></span> <span data-ttu-id="c2634-111">Il peut être de 1 à 20 caractères dans Microsoft Access espaces de travail et il peuvent inclure des caractères alphabétiques, accentuées, chiffres, espaces et symboles à l’exception de : » (guillemets) / (barre oblique), \\ barre oblique inverse (), \[ \] (crochets) , : (deux-points), | (canal), \< (moins-signe supérieur), \> (supérieur-signe supérieur), signe plus (+), = (signe égal), (point-virgule), (virgule) ?</span><span class="sxs-lookup"><span data-stu-id="c2634-111">It can be 1–20 characters long in Microsoft Access workspaces and it can include alphabetic characters, accented characters, numbers, spaces, and symbols except for: " (quotation marks), / (forward slash), \\ (backslash), \[ \] (brackets), : (colon), | (pipe), \< (less-than sign), \> (greater-than sign), + (plus sign), = (equal sign), ; (semicolon), , ( comma), ?</span></span> <span data-ttu-id="c2634-112">(point d’interrogation), \* astérisque (\*), des espaces et les caractères de contrôle (ASCII 00 à ASCII 31).</span><span class="sxs-lookup"><span data-stu-id="c2634-112">(question mark), \* (asterisk), leading spaces, and control characters (ASCII 00 to ASCII 31).</span></span>


> [!NOTE]
> <P><span data-ttu-id="c2634-p103">[!REMARQUE] Définissez des mots de passe forts qui combinent des lettres minuscules et majuscules, des nombres et des symboles. Les mots de passe faibles ne regroupent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : Maison27. Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.</span><span class="sxs-lookup"><span data-stu-id="c2634-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span></P>



<span data-ttu-id="c2634-118">Par défaut, la propriété **DefaultUser** est définie sur « admin » et la propriété **DefaultPassword** est définie sur une chaîne nulle ("").</span><span class="sxs-lookup"><span data-stu-id="c2634-118">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="c2634-p104">En règle générale, les noms d'utilisateur ne respectent pas la casse. Toutefois, si vous recréez un compte d'utilisateur qui a été supprimé ou créé dans un autre groupe de travail, les minuscules et les majuscules du nom d'utilisateur doivent correspondre exactement à celles du nom d'origine. Les mots de passe respectent la casse.</span><span class="sxs-lookup"><span data-stu-id="c2634-p104">User names aren't usually case-sensitive; however, if you're re-creating a user account that was deleted or created in a different workgroup, the user name must be an exact case-sensitive match of the original name. Passwords are case-sensitive.</span></span>

<span data-ttu-id="c2634-p105">En règle générale, vous utilisez la méthode **CreateWorkspace** pour créer un objet **Workspace** en fonction d'un nom d'utilisateur et d'un mot de passe spécifiques. Toutefois, pour des raisons de compatibilité descendante avec les versions antérieures et de commodité lorsque vous n'implémentez pas de base de données sécurisée, le moteur de base de données Microsoft Access crée automatiquement un objet **Workspace** par défaut s'il n'est pas encore ouvert. Dans ce cas, les valeurs des propriétés **DefaultUser** et **DefaultPassword** définissent l'utilisateur et le mot de passe correspondant à l'objet **Workspace** par défaut.</span><span class="sxs-lookup"><span data-stu-id="c2634-p105">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="c2634-124">Pour appliquer cette propriété, vous devez la définir avant d'appeler des méthodes DAO.</span><span class="sxs-lookup"><span data-stu-id="c2634-124">For this property to take effect, you should set it before calling any DAO methods.</span></span>

