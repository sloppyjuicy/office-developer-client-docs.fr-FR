---
title: Propriété DBEngine.DefaultPassword (DAO)
TOCTitle: DefaultPassword Property
ms:assetid: 189e34f3-d573-c75f-8be2-d98c50df8a52
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845616(v=office.15)
ms:contentKeyID: 48543478
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 705bd14208b3a6b07b7d5adddfc4f1fdf36928c5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924602"
---
# <a name="dbenginedefaultpassword-property-dao"></a><span data-ttu-id="9d51e-102">Propriété DBEngine.DefaultPassword (DAO)</span><span class="sxs-lookup"><span data-stu-id="9d51e-102">DBEngine.DefaultPassword property (DAO)</span></span>


<span data-ttu-id="9d51e-103">**S’applique à**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9d51e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9d51e-p101">Définit le mot de passe servant à créer l'objet **Workspace** par défaut lors de son initialisation. Valeur de type **String** en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="9d51e-p101">Sets the password used to create the default **Workspace** when it is initialized. Read/write **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d51e-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d51e-106">Syntax</span></span>

<span data-ttu-id="9d51e-107">*expression* . DefaultPassword</span><span class="sxs-lookup"><span data-stu-id="9d51e-107">*expression* .DefaultPassword</span></span>

<span data-ttu-id="9d51e-108">*expression* Variable qui représente un objet **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="9d51e-108">*expression* A variable that represents a **DBEngine** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d51e-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d51e-109">Remarks</span></span>

<span data-ttu-id="9d51e-p102">La valeur de la propriété **DefaultPassword** est une donnée de type String qui peut contenir jusqu'à 20 caractères. Elle accepte tous les caractères, à l'exception du caractère ASCII 0.</span><span class="sxs-lookup"><span data-stu-id="9d51e-p102">The setting for **DefaultPassword** is a String data type that can be up to 20 characters long. It can contain any character except ASCII 0.</span></span>


> [!NOTE]
> <span data-ttu-id="9d51e-p103">[!REMARQUE] Définissez des mots de passe forts qui combinent des lettres minuscules et majuscules, des nombres et des symboles. Les mots de passe faibles ne regroupent pas ces éléments. Mot de passe fort : Y6dh!et5. Mot de passe faible : Maison27. Utilisez un mot de passe fort dont vous pouvez vous souvenir sans devoir le noter.</span><span class="sxs-lookup"><span data-stu-id="9d51e-p103">Use strong passwords that combine upper- and lowercase letters, numbers, and symbols. Weak passwords don't mix these elements. Strong password: Y6dh!et5. Weak password: House27. Use a strong password that you can remember so that you don't have to write it down.</span></span>

<span data-ttu-id="9d51e-117">Par défaut, la propriété **DefaultUser** est définie sur « admin » et la propriété **DefaultPassword** est définie sur une chaîne nulle ("").</span><span class="sxs-lookup"><span data-stu-id="9d51e-117">By default, the **DefaultUser** property is set to "admin" and the **DefaultPassword** property is set to a zero-length string ("").</span></span>

<span data-ttu-id="9d51e-p104">En règle générale, vous utilisez la méthode **CreateWorkspace** pour créer un objet **Workspace** en fonction d'un nom d'utilisateur et d'un mot de passe spécifiques. Toutefois, pour des raisons de compatibilité descendante avec les versions antérieures et de commodité lorsque vous n'implémentez pas de base de données sécurisée, le moteur de base de données Microsoft Access crée automatiquement un objet **Workspace** par défaut s'il n'est pas encore ouvert. Dans ce cas, les valeurs des propriétés **DefaultUser** et **DefaultPassword** définissent l'utilisateur et le mot de passe correspondant à l'objet **Workspace** par défaut.</span><span class="sxs-lookup"><span data-stu-id="9d51e-p104">Typically, you use the **CreateWorkspace** method to create a **Workspace** object with a given user name and password. However, for backward compatibility with earlier versions and for convenience when you don't implement a secured database, the Microsoft Access database engine automatically creates a default **Workspace** object when needed if one isn't already open. In this case, the **DefaultUser** and **DefaultPassword** property values define the user and password for the default **Workspace** object.</span></span>

<span data-ttu-id="9d51e-121">Pour appliquer cette propriété, vous devez la définir avant d'appeler des méthodes DAO.</span><span class="sxs-lookup"><span data-stu-id="9d51e-121">For this property to take effect, you should set it before calling any DAO methods.</span></span>

