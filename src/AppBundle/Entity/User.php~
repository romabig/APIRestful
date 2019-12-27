<?php
namespace AppBundle\Entity;

use Doctrine\ORM\Mapping as ORM;

/**
 * @ORM\Entity()
 * @ORM\Table(name="users")
 * @ORM\HasLifecycleCallbacks
 */
class User
{
    /**
     * @ORM\Id
     * @ORM\Column(type="integer")
     * @ORM\GeneratedValue
     */
    protected $id;

    /**
     * @ORM\Column(type="string")
     */
    protected $firstname;

    /**
     * @ORM\Column(type="string")
     */
    protected $lastname;

    /**
     * @ORM\Column(type="datetime")
     */
    protected $creationdate;

    /**
     * @ORM\Column(type="datetime", nullable=true)
     */
    protected $updatedate;

//    public function __construct()
//    {
//        $this->creationdate = new \DateTime();
//    }

    public function getId()
    {
        return $this->id;
    }

    public function setId($id)
    {
        $this->id = $id;
    }

    public function getFirstname()
    {
        return $this->firstname;
    }

    public function setFirstname($firstname)
    {
        $this->firstname = $firstname;
    }

    public function getLastname()
    {
        return $this->lastname;
    }

    public function setLastname($lastname)
    {
        $this->lastname = $lastname;
    }

    public function getCreationdate()
    {
        return $this->creationdate;
    }

    public function setCreationdate($creationdate)
    {
        $this->creationdate = $creationdate;
    }

    public function getUpdatedate()
    {
        return $this->updatedate;
    }

    public function setUpdatedate($updatedate)
    {
        $this->updatedate = $updatedate;
    }

    /**
     * Gets triggered only on insert

     * @ORM\PrePersist
     */
    public function onPrePersist()
    {
        $this->creationdate = new \DateTime("now");
    }

    /**
     * Gets triggered every time on update

     * @ORM\PreUpdate
     */
    public function onPreUpdate()
    {
        $this->updatedate = new \DateTime("now");
    }
}
